idf_component_register(SRCS "lib/mongoose.c"
                       INCLUDE_DIRS "lib"
                       REQUIRES lwip mbedtls esp_timer app_update)
component_compile_options(-DMG_TLS=MG_TLS_BUILTIN -DMG_IO_SIZE=500 -DMG_ENABLE_MD5=0 -DMG_ENABLE_LWIP=1 -DMG_ARCH=MG_ARCH_ESP32)
target_compile_definitions(${COMPONENT_LIB} PRIVATE MG_ENABLE_MBEDTLS=1 MG_ARCH=MG_ARCH_ESP32)
