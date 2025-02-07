cmake_minimum_required(VERSION 3.10...3.18)

add_subdirectory(basalt-headers EXCLUDE_FROM_ALL)
add_subdirectory(apriltag EXCLUDE_FROM_ALL)

# fix aprilgrid
target_compile_options(apriltag PRIVATE "-Wno-unused-private-field")
