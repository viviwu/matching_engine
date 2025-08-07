add_subdirectory(latency)
add_subdirectory(perf)

add_test(NAME unit
        COMMAND "unit/ut_all_or_none.cpp"
)
#CMake Error at test/CMakeLists.txt:3 (add_test):
#add_test called with incorrect number of arguments
