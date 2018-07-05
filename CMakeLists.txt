cmake_minimum_required(VERSION 3.5)

project(console_bridge_vendor)

find_package(ament_cmake REQUIRED)

macro(build_console_bridge)
  set(extra_cmake_args)
  if(DEFINED CMAKE_BUILD_TYPE)
    list(APPEND extra_cmake_args -DCMAKE_BUILD_TYPE=${CMAKE_BUILD_TYPE})
  endif()

  include(ExternalProject)
  ExternalProject_Add(console_bridge-0.4.0
    URL https://github.com/ros/console_bridge/archive/0.4.0.tar.gz
    URL_MD5 19a7b3ee7e99e41c1abd5c005418f50a
    TIMEOUT 600
    CMAKE_ARGS
      -DCMAKE_INSTALL_PREFIX=${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}_install
      ${extra_cmake_args}
      -Wno-dev
  )

  # The external project will install to the build folder, but we'll install that on make install.
  install(
    DIRECTORY
      ${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}_install/
    DESTINATION
      ${CMAKE_INSTALL_PREFIX}
  )
endmacro()

find_package(console_bridge QUIET)

if(NOT console_bridge_FOUND OR "${console_bridge_VERSION}" VERSION_LESS 0.4.0)
  build_console_bridge()
endif()

# this ensures that the package has an environment hook setting the PATH
ament_package()
