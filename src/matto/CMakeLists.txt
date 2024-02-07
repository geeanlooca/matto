include(GenerateExportHeader)

add_library(matto fen.cpp)
target_include_directories(matto PUBLIC $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include> $<BUILD_INTERFACE:${PROJECT_BINARY_DIR}/include>)
target_include_directories(matto PUBLIC ${CMAKE_BINARY_DIR}/include/matto)

# print the ${CMAKE_BINARY_DIR}/include
message(STATUS "CMAKE_BINARY_DIR: ${CMAKE_BINARY_DIR}/include")

target_compile_features(matto PUBLIC cxx_std_20)
generate_export_header(matto EXPORT_FILE_NAME ${PROJECT_BINARY_DIR}/include/matto/matto_export.hpp)


