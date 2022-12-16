add_subdirectory("pbrt-v4") 

set (PBRT_HEADER_DIR
    ${PROJECT_SOURCE_DIR}/3rd/pbrt-v4/src/pbrt
    PARENT_SCOPE 
  )  


set (PBRT_DEFINITIONS ${PBRT_DEFINITIONS} PARENT_SCOPE)

message(STATUS "lll" ${PBRT_DEFINITIONS})
add_subdirectory("entt") 