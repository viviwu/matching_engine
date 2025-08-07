cmake_minimum_required(VERSION 3.15)

project(
        "matching_engine"
        VERSION 0.1.0
        LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
#set(CMAKE_CXX_EXTENSIONS OFF)
#set(CMAKE_BUILD_TYPE Release)
set(CMAKE_INSTALL_PREFIX "${CMAKE_CURRENT_SOURCE_DIR}/install")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/lib")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/lib")

cmake_policy(SET CMP0167 NEW)
# 查找依赖包
find_package(Boost REQUIRED COMPONENTS system)
message(STATUS "Boost: ${Boost_DIR}")
include_directories( .
        src
        ${Boost_INCLUDE_DIRS}
)

FILE(GLOB_RECURSE BOOK_SRC src/book/*.h )
message(STATUS "BOOK_SRC: ${BOOK_SRC}")
FILE(GLOB_RECURSE SIMPLE_SRC src/simple/*.h src/simple/*.cpp)
message(STATUS "SIMPLE_SRC: ${SIMPLE_SRC}")

#AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/src/book BOOK_SRC)
#message(STATUS "BOOK_SRC: ${BOOK_SRC}")

add_subdirectory(examples)
add_subdirectory(src)
add_subdirectory(test)
