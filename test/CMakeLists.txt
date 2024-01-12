# 包含gtest库
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})

add_executable(test_code test.cpp)
target_link_libraries(test_code GTest::GTest GTest::Main)

# 添加测试
add_test(NAME MyCodeTest COMMAND test_code)