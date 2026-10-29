cmake_minimum_required(VERSION 3.16)

project(Trabalho6 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(OpenCV_DIR "$ENV{HOME}/OpenCV/opencv-build/install/lib/cmake/opencv5")

find_package(OpenCV REQUIRED COMPONENTS core imgcodecs highgui imgproc)

add_executable(trabalho6 src/main.cpp)

target_include_directories(trabalho6 PRIVATE ${OpenCV_INCLUDE_DIRS})

target_link_libraries(trabalho6 PRIVATE ${OpenCV_LIBS})
