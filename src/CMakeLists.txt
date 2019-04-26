cmake_minimum_required(VERSION 2.8)

project(myProject)

set(CMAKE_CXX_FLAGS "-Wall -Wextra -Wpedantic -std=c++14")
set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake-modules)

include(CodeCoverage)
APPEND_COVERAGE_COMPILER_FLAGS()
set(COVERAGE_LCOV_EXCLUDES '${CMAKE_CURRENT_BINARY_DIR}/*' '/usr/*' '${PROJECT_SOURCE_DIR}/test/*')
SETUP_TARGET_FOR_COVERAGE_LCOV(NAME coverage EXECUTABLE runtests)

enable_testing()

add_subdirectory(main)
add_subdirectory(test)

