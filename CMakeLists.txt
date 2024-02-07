cmake_minimum_required(VERSION 3.19)


if (NOT DEFINED CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 20)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
endif()


# avoid conflicts when compiling with PCH
set(CMAKE_CXX_EXTENSIONS OFF)

include(cmake/ConfigureVcpkg.cmake)





project(matto VERSION 0.1.0 LANGUAGES CXX)

include(cmake/PreventInSourceBuilds.cmake)

add_subdirectory(src)