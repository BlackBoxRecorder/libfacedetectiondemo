cmake_minimum_required (VERSION 3.8)

project ("libfacedetectiondemo")

find_package(OpenCV REQUIRED)

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/libfacedetection/include 
    ${OpenCV_INCLUDE_DIRS}
)

link_directories(${CMAKE_CURRENT_SOURCE_DIR}/libfacedetection/lib)

add_executable (libfacedetectiondemo  "libfacedetectiondemo.cpp" )

TARGET_LINK_LIBRARIES(libfacedetectiondemo ${OpenCV_LIBS} facedetection)


