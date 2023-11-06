cmake_minimum_required(VERSION 3.27)

project(ZoneDetect VERSION 1.0.0)

find_package(shapelib)

add_subdirectory(library)
add_subdirectory(database/builder)

add_executable(demo
	demo.c
)

target_include_directories(demo
	PRIVATE library
)

target_link_libraries(demo
	PRIVATE zonedetect
)

add_dependencies(demo zonedetect-builder)
