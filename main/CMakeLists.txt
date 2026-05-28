idf_component_register(
    SRCS "main.cpp" "clock_settings.cpp" "clock_buttons.cpp" "clock_display.cpp" "clock_menu.cpp" "clock_ethernet.cpp" "clock_alarm.cpp" "clock_protocol.cpp" "clock_modes.cpp"
    INCLUDE_DIRS "."
    REQUIRES 
    	led_panel 
    	DS3231 
    	DS18B20 
    	esp_event 
    	esp_netif 
    	esp_eth 
    	driver 
    	lwip 
    	espressif__w5500 
    	esp_driver_i2s         
    	esp_https_ota
        esp_http_client
        app_update
        esp_wifi
        nvs_flash
)

target_compile_features(${COMPONENT_LIB} PRIVATE cxx_std_17)