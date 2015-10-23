set(TARGET_NAME GameHomework)

file(GLOB SRC_FILES *.cpp)

add_executable(${TARGET_NAME} ${SRC_FILES})

target_include_directories(${TARGET_NAME}
                          ${BAR_INCLUDE_DIRS}
                          "${CMAKE_SOURCE_DIR}/include"
                          "${FOO_INCLUDE_DIR}"
)

target_link_libraries(${TARGET_NAME} "${FOO_LIBRARY}" ${BAR_LIBRARIES})

install (TARGETS ${TARGET_NAME} DESTINATION TARGET_FOLDER)
