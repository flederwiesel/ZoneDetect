find_package(shapelib)

add_executable(zonedetect-builder
	builder.cpp
)

target_link_libraries(zonedetect-builder
    PRIVATE shp
)
