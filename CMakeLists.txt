cmake_minimum_required(VERSION 3.17)
project(Shahu)

set(CMAKE_CXX_STANDARD 14)

add_executable(Shahu main.cpp shahu.h src/HelloWorld.cpp src/controllers/Controller.h src/views/View.h src/views/MainMenu.h src/views/MainMenu.cpp)


INCLUDE_DIRECTORIES(  allegro/include )
LINK_DIRECTORIES(  allegro/lib )

file(GLOB LIBRARIES "allegro/lib/*.dll.a")
message("LIBRARIES = ${LIBRARIES}")

TARGET_LINK_LIBRARIES(Shahu  ${LIBRARIES})