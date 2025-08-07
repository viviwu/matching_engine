
add_executable(latency
    lt_order_book.cpp
    clock_gettime.h
    ${BOOK_SRC} ${SIMPLE_SRC}
)


#target_link_libraries(latency PRIVATE ${Boost_LIBRARIES})