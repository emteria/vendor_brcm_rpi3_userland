SET( MMAL_TOP ../../.. )

include_directories(${PROJECT_SOURCE_DIR}/host_applications/linux/libs/bcm_host/include)

SET( MMALPLAY_TOP ${MMAL_TOP}/host_applications/vmcs/test_apps/mmalplay )
add_executable(mmalplay ${MMALPLAY_TOP}/playback.c ${MMALPLAY_TOP}/mmalplay.c)
#target_link_libraries(mmalplay mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmalplay -Wl,--whole-archive mmal_components containers -Wl,--no-whole-archive mmal_core)
#target_link_libraries(mmalplay vcos)
target_link_libraries(mmalplay mmal bcm_host vcos)

SET( MMALCAM_TOP ${MMAL_TOP}/host_applications/vmcs/test_apps/mmalcam )
add_executable(mmalcam ${MMALCAM_TOP}/viewfinder.c ${MMALCAM_TOP}/mmalcam.c)
#target_link_libraries(mmalcam mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmalcam -Wl,--whole-archive mmal_components -Wl,--no-whole-archive mmal_core)
#target_link_libraries(mmalcam vcos)
target_link_libraries(mmalcam mmal bcm_host vcos)

SET( MMALEXAMPLES_TOP ${MMAL_TOP}/interface/mmal/test/examples )
add_executable(mmal_example_connections ${MMALEXAMPLES_TOP}/example_connections.c)
#target_link_libraries(mmal_example_connections mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmal_example_connections -Wl,--whole-archive mmal_components -Wl,--no-whole-archive mmal_core)
target_link_libraries(mmal_example_connections mmal bcm_host)
add_executable(mmal_example_graph ${MMALEXAMPLES_TOP}/example_graph.c)
#target_link_libraries(mmal_example_graph mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmal_example_graph -Wl,--whole-archive mmal_components -Wl,--no-whole-archive mmal_core)
target_link_libraries(mmal_example_graph mmal bcm_host)
add_executable(mmal_example_basic_1 ${MMALEXAMPLES_TOP}/example_basic_1.c)
#target_link_libraries(mmal_example_basic_1 mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmal_example_basic_1 -Wl,--whole-archive mmal_components -Wl,--no-whole-archive mmal_core)
target_link_libraries(mmal_example_basic_1 mmal bcm_host)
add_executable(mmal_example_basic_2 ${MMALEXAMPLES_TOP}/example_basic_2.c)
#target_link_libraries(mmal_example_basic_2 mmal_core mmal_util bcm_host mmal_vc_client)
#target_link_libraries(mmal_example_basic_2 -Wl,--whole-archive mmal_components -Wl,--no-whole-archive mmal_core)
target_link_libraries(mmal_example_basic_2 mmal bcm_host)
