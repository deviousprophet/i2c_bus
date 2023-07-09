if(IDF_VERSION_MAJOR GREATER_EQUAL 5)
    idf_component_register(
        SRCS "i2c_bus.c"
        INCLUDE_DIRS "include"
        REQUIRES driver
    )
    target_compile_options(${COMPONENT_LIB} PRIVATE -Wno-format)
else()
    idf_component_register(
        SRCS "i2c_bus.c"
        INCLUDE_DIRS "include"
    )
endif()
