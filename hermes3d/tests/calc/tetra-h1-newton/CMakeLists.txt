project(calc-tetra-h1-newton)
add_executable(${PROJECT_NAME}	tetra-newton.cpp)

include (${hermes3d_SOURCE_DIR}/CMake.common)
set_common_target_properties(${PROJECT_NAME})

# Tests

set(BIN ${PROJECT_BINARY_DIR}/${PROJECT_NAME})
add_test(${PROJECT_NAME}-1 ${BIN} ${MESHES_DIR}/mesh3d/tetra1-ref.mesh3d 2)
add_test(${PROJECT_NAME}-2 ${BIN} ${MESHES_DIR}/mesh3d/tetra1.mesh3d 2)
