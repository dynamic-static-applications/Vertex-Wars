
#==========================================
#  Copyright (c) 2020 dynamic_static
#    Patrick Purcell
#      Licensed under the MIT license
#    http://opensource.org/licenses/MIT
#==========================================

cmake_minimum_required(VERSION 3.3 FATAL_ERROR)
project(vertex-wars VERSION 1.0.0)
set(CMAKE_CXX_STANDARD 17)

# Dependencies
set(external "${CMAKE_CURRENT_LIST_DIR}/external/")
include("${external}/dynamic_static.build.cmake")
include("${external}/dynamic_static.graphics.cmake")

set(includeDirectory "${CMAKE_CURRENT_LIST_DIR}/include/")
set(includePath "${includeDirectory}/vertex-wars/")
set(sourcePath "${CMAKE_CURRENT_LIST_DIR}/source/vertex-wars/")
dst_add_executable(
    target vertex-wars
    linkLibraries dynamic_static.graphics
    includeDirectories "${includeDirectory}"
    includeFiles
        "${includePath}/defines.hpp"
    sourceFiles
        "${sourcePath}/main.cpp"
)
