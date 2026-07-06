cmake_minimum_required(VERSION 3.10)

project(Rasterizer)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenCV REQUIRED)

add_executable(Rasterizer
    main.cpp
    rasterizer.cpp
    Triangle.cpp
)

target_include_directories(Rasterizer PRIVATE
    ${OpenCV_INCLUDE_DIRS}
)

target_link_libraries(Rasterizer PRIVATE
    ${OpenCV_LIBS}
)
