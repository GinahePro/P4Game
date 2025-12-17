cmake_minimum_required(VERSION 3.12)


project(P4Game)


add_subdirectory(vendors/glfw/glfw-3.4)
find_package(OpenGL REQUIRED)

add_executable(P4Game src/main.cpp)
target_include_directories(P4Game PUBLIC ${OPENGL_INCLUDE_DIRS} )
target_link_libraries(P4Game glfw)
target_link_libraries(P4Game OpenGL::GL)
