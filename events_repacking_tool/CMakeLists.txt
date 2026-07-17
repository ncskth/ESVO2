cmake_minimum_required(VERSION 2.8.3)
project(events_repacking_tool)

find_package(Eigen3 REQUIRED)
find_package(catkin_simple REQUIRED)

catkin_simple()

add_message_files(FILES V_ba_bg.msg)
generate_messages(DEPENDENCIES dvs_msgs)

cs_add_executable(EventMessageEditor src/EventMessageEditor.cpp)
target_link_libraries(EventMessageEditor ${catkin_LIBARIES})