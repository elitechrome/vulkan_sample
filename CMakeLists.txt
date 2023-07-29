cmake_minimum_required(VERSION 3.13)
project(vulkan_sample)

set(CMAKE_CXX_STANDARD 17)
find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)

include(AddVulkanProject.cmake)

# add_executable(vulkan_sample main.cpp)
file(GLOB sources *.cpp)
add_vulkan_project(vulkan_sample "${sources}")