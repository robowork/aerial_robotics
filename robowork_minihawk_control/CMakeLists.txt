cmake_minimum_required(VERSION 2.8.3)
project(robowork_minihawk_control)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

roslaunch_add_file_check(launch)

# catkin_install_python(PROGRAMS
#                         scripts/init_minihawk
#                       DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY config launch scripts
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
