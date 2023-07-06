idf_component_register(
    SRCS "i2c_bus.c"
    INCLUDE_DIRS "include"
    REQUIRES "driver"
)

target_compile_options(${COMPONENT_LIB} PRIVATE "-Wno-format" "-Wno-maybe-uninitialized" "-Wno-incompatible-pointer-types")
