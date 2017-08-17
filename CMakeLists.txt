cmake_minimum_required(VERSION 2.8.3)
project(image_publisher)
find_package(catkin REQUIRED cv_bridge genmsg image_transport sensor_msgs)

catkin_package()

include_directories()

add_executable(image_publisher src/image_publisher.cpp)
target_link_libraries(image_publisher ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})
