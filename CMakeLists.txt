cmake_minimum_required(VERSION 2.8.3)
project(simple_image_publisher)
find_package(catkin REQUIRED cv_bridge image_transport sensor_msgs)

catkin_package()

find_package(OpenCV REQUIRED)

include_directories(
  include
  ${OpenCV_INCLUDE_DIRS}
)

add_executable(image_publisher src/image_publisher.cpp)
target_link_libraries(image_publisher ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})
