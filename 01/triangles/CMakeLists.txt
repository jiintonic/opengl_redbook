set(TARGET_NAME triangles)

set(SRC_FILES triangles.cpp ../../lib/LoadShaders.cpp)
# file(GLOB SRC_FILES *.cpp ../lib/*.cpp)

add_executable(${TARGET_NAME} ${SRC_FILES})

target_include_directories(${TARGET_NAME} PRIVATE
                          ${GLEW_INCLUDE_DIRS}
                          ${GLM_INCLUDE_DIRS}
                          "${CMAKE_SOURCE_DIR}/include"
                          "${OPENGL_INCLUDE_DIR}"
)

target_link_libraries(${TARGET_NAME}
                      ${GLEW_LIBRARIES}
                      ${OPENGL_LIBRARIES}
                      "${GLUT_LIBRARY}"
)

install (TARGETS ${TARGET_NAME} DESTINATION output)
