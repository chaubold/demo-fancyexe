cmake_minimum_required(VERSION 2.8)
project(fancyexe CXX)

file(GLOB_RECURSE SOURCES *.cpp)
file(GLOB_RECURSE HEADERS *.h)

include_directories(${PROJECT_SOURCE_DIR}/../ext/libfoo/libfoo/include ${PROJECT_SOURCE_DIR}/../ext/libbar/libbar/include)

add_executable(fancyexe ${SOURCES} ${HEADERS})
target_link_libraries(fancyexe libfoo libbar)

