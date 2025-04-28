cmake_minimum_required(VERSION 3.31)
project(game)

add_subdirectory(luna ${CMAKE_CURRENT_BINARY_DIR}/luna)

add_executable(${PROJECT_NAME} WIN32)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_23)
target_sources(${PROJECT_NAME} PRIVATE source/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE luna)

