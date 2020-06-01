set(TARGET_NAME driver_motion_pose)

add_library(${TARGET_NAME} SHARED
  driverlog.cpp
  driverlog.h
  motion_pose.cpp
)

add_definitions(-DDRIVER_SAMPLE_EXPORTS)

target_link_libraries(${TARGET_NAME}
  ${OPENVR_LIBRARIES}
  ${CMAKE_DL_LIBS}
)

setTargetOutputDirectory(${TARGET_NAME})
