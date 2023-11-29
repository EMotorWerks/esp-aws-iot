# Include coreJSON library's source and header path variables.
include( "${CMAKE_CURRENT_LIST_DIR}/coreJSON/jsonFilePaths.cmake" )

idf_component_register(
    SRCS
        "${JSON_SOURCES}"
    INCLUDE_DIRS
        "${JSON_INCLUDE_PUBLIC_DIRS}"
        "."
)

set_source_files_properties(
"${CMAKE_CURRENT_LIST_DIR}/coreJSON/source/core_json.c"
PROPERTIES COMPILE_FLAGS "-w")
