#
# Copyright (C) 2022-2024, HENSOLDT Cyber GmbH
# 
# SPDX-License-Identifier: GPL-2.0-or-later
#
# For commercial licensing, contact: info.cyber@hensoldt.net
#

function(BMP280_DeclareCAmkESComponent name)

DeclareCAmkESComponent(
    ${name}
    INCLUDES
    ${CMAKE_CURRENT_FUNCTION_LIST_DIR}/3rdParty/include
    SOURCES
    ${CMAKE_CURRENT_FUNCTION_LIST_DIR}/3rdParty/src/bmp280.c
    ${CMAKE_CURRENT_FUNCTION_LIST_DIR}/src/bmp280_rpc.c
    LIBS
    system_config
    lib_debug
    os_core_api
    i2c_client
)

endfunction()