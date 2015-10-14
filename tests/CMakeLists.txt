include_directories(${CMAKE_CURRENT_SOURCE_DIR}/..)

find_package(Check REQUIRED)
include_directories(${CHECK_INCLUDE_DIRS})

set(LIBS heap ${CHECK_LIBRARIES} m rt pthread)

add_executable(check_heap check_heap.c)
target_link_libraries(check_heap ${LIBS})

