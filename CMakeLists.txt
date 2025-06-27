cmake_minimum_required(VERSION 3.10)
project(Labirint)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(GLEW REQUIRED)
find_package(glm REQUIRED)
find_package(assimp REQUIRED)
find_package(OpenAL REQUIRED)

add_executable(labirint src/maze_game.cpp)
target_link_libraries(labirint OpenGL::GL glfw GLEW::GLEW assimp::assimp ${OPENAL_LIBRARY})
