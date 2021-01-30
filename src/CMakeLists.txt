file(GLOB CPP_SOURCES "*.cpp")

add_executable(rkvMTv2 ${CPP_SOURCES})
target_compile_features(rkvMTv2 PUBLIC cxx_std_17)
set_target_properties(rkvMTv2 PROPERTIES CXX_EXTENSIONS OFF
										  RUNTIME_OUTPUT_DIRECTORY "${PROJECT_BINARY_DIR}")
target_link_libraries(rkvMTv2 RKV1 -static)