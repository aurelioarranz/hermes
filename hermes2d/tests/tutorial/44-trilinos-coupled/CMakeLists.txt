if (NOT H2D_REAL)
    return()
endif (NOT H2D_REAL)

if (WITH_TRILINOS)

project(tutorial-44-trilinos-coupled)

add_executable(${PROJECT_NAME} main.cpp)
include (../../CMake.common)

set(BIN ${PROJECT_BINARY_DIR}/${PROJECT_NAME})
add_test(tutorial-44-trilinos-coupled ${BIN})
set_tests_properties(tutorial-44-trilinos-coupled PROPERTIES LABELS slow)

endif (WITH_TRILINOS)

