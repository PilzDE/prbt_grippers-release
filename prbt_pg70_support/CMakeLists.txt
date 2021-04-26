cmake_minimum_required(VERSION 3.0.2)
project(prbt_pg70_support)

find_package(catkin REQUIRED)
catkin_package()

#############
## Install ##
#############
install(DIRECTORY urdf DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
