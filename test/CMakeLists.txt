set(GTEST_SHUFFLE 1)

add_executable(
    cpp-test
    main.cpp
    test.cpp
    $<TARGET_OBJECTS:pidController>
)

target_include_directories(cpp-test PUBLIC ../vendor/googletest/googletest/include)
target_link_libraries(cpp-test PUBLIC gtest)

include_directories(${CMAKE_SOURCE_DIR}/include)