cmake_minimum_required(VERSION 3.30)
project(game)

add_subdirectory(luna)

add_executable(${PROJECT_NAME} WIN32
  source/main.cpp
)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_20)
target_link_libraries(${PROJECT_NAME} PRIVATE luna)
