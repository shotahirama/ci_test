project(samplegtest)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread")

find_package(GTest REQUIRED)

include_directories(${GTEST_INCLUDE_DIRS})
add_executable(sample sample.cpp)
target_link_libraries(sample ${GTEST_BOTH_LIBRARIES})
enable_testing()
