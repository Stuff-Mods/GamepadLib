project(GamepadLib)
FILE(GLOB_RECURSE GamepadLibSources CONFIGURE_DEPENDS ${PROJECT_SOURCE_DIR} *.h *.cpp)
add_library(GamepadLib SHARED ${GamepadLibSources})
target_compile_definitions(GamepadLib PRIVATE GAMEPAD_LISTENER_IMP)
target_include_directories(GamepadLib PUBLIC GamepadHeaders)
target_compile_features(GamepadLib PRIVATE cxx_std_17)
