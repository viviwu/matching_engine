
file(GLOB DEPTH_FEED_PUBLISHER_SRC *.h *.cpp)
message(STATUS "DEPTH_FEED_PUBLISHER_SRC: ${DEPTH_FEED_PUBLISHER_SRC}")

add_executable(depth_feed_publisher
        ${DEPTH_FEED_PUBLISHER_SRC}
        ${BOOK_SRC} ${SIMPLE_SRC}
)

target_include_directories(depth_feed_publisher PRIVATE
        ../../QuickFAST/src
)
target_link_directories(depth_feed_publisher PRIVATE ${Boost_LIBRARY_DIRS} )