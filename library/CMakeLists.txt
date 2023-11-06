add_library(zonedetect SHARED
	zonedetect.c
)

set_target_properties(zonedetect PROPERTIES
	C_STANDARD 99
	C_STANDARD_REQUIRED ON
	C_EXTENSIONS OFF
	COMPILE_WARNING_AS_ERROR ON
	POSITION_INDEPENDENT_CODE ON
	VERSION ${PROJECT_VERSION}   # Product version
	SOVERSION 1.0.0 # [GNU Library interface version](https://www.gnu.org/software/libtool/manual/html_node/Updating-version-info.html)
)

target_compile_definitions(zonedetect
	PRIVATE BUILD_LIBZONETEDECT
)

#target_link_libraries(zonedetect
#    INTERFACE m
#)
