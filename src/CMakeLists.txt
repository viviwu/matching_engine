#cmake_minimum_required(VERSION 3.15)
#project(liquibook)
#message(STATUS "BOOK_SRC: ${BOOK_SRC}")
include_directories(. )
add_executable(liquibook_desc
        book/main.cpp
        ${BOOK_SRC}
)
