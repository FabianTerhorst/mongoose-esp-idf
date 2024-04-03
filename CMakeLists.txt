idf_component_register(SRCS "mongoose/mongoose.c"
                       INCLUDE_DIRS "mongoose"
                       REQUIRES lwip mbedtls esp_timer)
component_compile_options(-DMG_TLS=MG_TLS_MBED)
target_compile_definitions(${COMPONENT_LIB} PRIVATE MG_ENABLE_MBEDTLS=1)
