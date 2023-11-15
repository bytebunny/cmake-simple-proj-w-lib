project( my-lib VERSION 1.0 LANGUAGES CXX )

set( lib_dir_name "my_lib" )

add_library( ${PROJECT_NAME} STATIC )

target_include_directories(${PROJECT_NAME} PUBLIC
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  $<INSTALL_INTERFACE:include> )

target_sources( ${PROJECT_NAME}
  PRIVATE
  src/foo.cpp
  src/foo.hpp
  src/add_one.cpp )
