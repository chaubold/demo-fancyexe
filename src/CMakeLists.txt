cmake_minimum_required(VERSION 2.8)
project(fancyexe CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

file(GLOB_RECURSE SOURCES *.cpp)
file(GLOB_RECURSE HEADERS *.h)

#include_directories(${PROJECT_SOURCE_DIR}/include)

add_executable(fancyexe ${SOURCES} ${HEADERS})
target_link_libraries(fancyexe ${CONAN_LIBS})

