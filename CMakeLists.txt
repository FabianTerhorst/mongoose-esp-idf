idf_component_register(SRCS "mongoose/mongoose.c"
                       INCLUDE_DIRS "mongoose"
                       REQUIRES lwip mbedtls esp_timer)
component_compile_options(-DMG_TLS=MG_TLS_MBED -DMG_IO_SIZE=500 -DMG_ENABLE_MD5=0 -DMG_ENABLE_LWIP=1)
target_compile_definitions(${COMPONENT_LIB} PRIVATE MG_ENABLE_MBEDTLS=1)
