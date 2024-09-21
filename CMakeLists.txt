project(GLFW)

add_library(GLFW STATIC
    include/GLFW/glfw3.h
    include/GLFW/glfw3native.h
    src/internal.h
    src/platform.h
    src/mappings.h
    src/context.c
    src/init.c
    src/input.c
    src/monitor.c
    src/platform.c
    src/vulkan.c
    src/window.c
    src/egl_context.c
    src/osmesa_context.c
    src/null_platform.h
    src/null_joystick.h
    src/null_init.c
    src/null_monitor.c
    src/null_window.c
    src/null_joystick.c
    src/cocoa_init.m
    src/cocoa_joystick.h
    src/cocoa_joystick.m
    src/cocoa_monitor.m
    src/cocoa_platform.h
    src/cocoa_time.h
    src/cocoa_time.c
    src/cocoa_window.m
)

set_target_properties(GLFW PROPERTIES
        RUNTIME_OUTPUT_DIRECTORY_DEBUG ${CMAKE_BINARY_DIR}/bin/Debug
        RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_BINARY_DIR}/bin/Release
        RUNTIME_OUTPUT_DIRECTORY_DIST ${CMAKE_BINARY_DIR}/bin/Dist
)