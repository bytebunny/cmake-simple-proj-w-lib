cmake_minimum_required( VERSION 3.23 )

project( cmake-simple-proj-w-lib VERSION 1.0 LANGUAGES CXX )

add_subdirectory( libs/my_lib )

add_executable( ${CMAKE_PROJECT_NAME} )

target_sources( ${CMAKE_PROJECT_NAME}
  PRIVATE
  src/main.cpp )

target_link_libraries( ${CMAKE_PROJECT_NAME} PRIVATE my-lib )
