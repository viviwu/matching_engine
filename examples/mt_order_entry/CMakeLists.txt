
project(mt_order_entry)

file(GLOB MT_ORDER_ENTRY_SRC *.h *.cpp)
message(STATUS "MT_ORDER_ENTRY_SRC: ${MT_ORDER_ENTRY_SRC}")

add_executable(mt_order_entry
        ${MT_ORDER_ENTRY_SRC}
        ${BOOK_SRC} ${SIMPLE_SRC}
)