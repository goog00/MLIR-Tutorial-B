set(ch_num 6)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
include_directories(${CMAKE_CURRENT_BINARY_DIR}/include)
add_subdirectory(include)
add_subdirectory(src)
add_executable(CH-${ch_num} "main.cpp")
target_link_libraries(CH-${ch_num} MLIRNorthStarDialect${ch_num} MLIRGPUDialect MLIRFuncDialect)
