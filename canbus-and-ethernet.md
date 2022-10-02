## CAN bus signals from IC:

|Signal ID|Length|Signal Name|
|---|---|---|
|0x20C|8|IC_Status|
|0x31C|2|IC_warningMatrix|
|0x32C|8|IC_info|
|0x38C|2|IC_faultMatrix|
|0x59C|8|IC_version|
|0x70C|8|IC_10Hz_Debug|

### IC_status:
|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|0|1|bool|IC_backlightOn|
|1|0|1|bool|IC_tegraAlive|
|2|0|1|bool|IC_tegraDisplayingUI|
|4|0|1|bool|IC_ackClusterPoweringOff|
|8|0|8|s8|IC_displayBrightness|
|16|0|8|u8, /10|IC_12vSupply|
|24|0|8|u8|IC_LEDBrightnessClass|

### IC_warningMatrix
|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|0|1|bool|IC_w001_CAN_RX|
|1|0|1|bool|IC_w002_CAN_TX|
|2|0|1|bool|IC_w003_CAN_ERR|
|3|0|1|bool|IC_w004_CAN_OVERRUN|
|4|0|1|bool|IC_w005_FIRMWARE|
|5|0|1|bool|IC_w006_FPGA_ERROR|
|6|0|1|bool|IC_w007_WATCHDOG_RESET|
|7|0|1|bool|IC_w008_MEMORY_ERROR|
|8|0|1|bool|IC_w009_SPI_OPEN|
|9|0|1|bool|IC_w010_SPI_READ|
|10|0|1|bool|IC_w011_CAN_RX_ERRCNT|
|11|0|1|bool|IC_w012_CAN_TX_ERRCNT|
|12|0|1|bool|IC_w013_OVERTEMP_OFF|
|13|0|1|bool|IC_w014_unused|
|14|0|1|bool|IC_w015_unused|
|15|0|1|bool|IC_w016_unused|

### IC_info:
|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|N/A|8|u8|Mux|
|8|10|8|u8|IC_buildType|
|16|10|16|u16|IC_buildConfigurationId|
|32|10|16|u16|IC_hardwareId|
|48|10|16|u16|IC_componentId|
|16|11|8|u8|IC_pcbaId|
|24|11|8|u8|IC_assemblyId|
|32|11|16|u16|IC_usageId|
|48|11|16|u16|IC_subUsageId|
|32|13|32|u32|IC_applicationCrc|
|16|16|8|u8|IC_FPGA_version|
|8|19|8|u8|IC_platformTyp|
|8|20|8|u8|IC_infoBootLdUdsProtocolVersion|
|32|20|32|u32|IC_bootloaderCrc|

### IC_faultMatrix:

|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|0|1|bool|IC_f001_unused|
|1|0|1|bool|IC_f002_unused|
|2|0|1|bool|IC_f003_unused|
|3|0|1|bool|IC_f004_unused|
|4|0|1|bool|IC_f005_unused|
|5|0|1|bool|IC_f006_unused|
|6|0|1|bool|IC_f007_unused|
|7|0|1|bool|IC_f008_unused|
|8|0|1|bool|IC_f009_unused|
|9|0|1|bool|IC_f010_unused|
|10|0|1|bool|IC_f011_unused|
|11|0|1|bool|IC_f012_unused|
|12|0|1|bool|IC_f013_unused|
|13|0|1|bool|IC_f014_unused|
|14|0|1|bool|IC_f015_unused|
|15|0|1|bool|IC_f016_unused|

### IC_version:

|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|0|8|u8|IC_platformType|
|8|0|8|u8|IC_platformMajorVersion|
|16|0|8|u8|IC_platformBranchOrigin|
|24|0|8|u8|IC_platformMaturity|
|32|0|8|u8|IC_componentMajorVersion|
|40|0|8|u8|IC_componentBranchOrigin|
|48|0|8|u8|IC_componentMaturity|
|56|0|8|u8|IC_componentHardwareRevision|

### IC_10Hz_Debug:

|Position|Index|Size|Type|Description|
|---|---|---|---|---|
|0|0|8|u8|IC_10Hz_state|
|8|0|8|u8|IC_10Hz_last_state|
|16|0|16|u16|IC_10Hz_fanDebug|
|32|0|1|bool|IC_10Hz_gatewayWakeLine|
|33|0|1|bool|IC_10HZ_gatewayResetLine|
|40|0|8|u8|IC_10HZ_CH_txectr|
|48|0|8|u8|IC_10Hz_CH_rxectr|

## Ethernet ports on IC:

|Port|Service|
|---|---|
|22|ssh|
|111|rpcbind|
|4130|QtCar VAPI|
|21576|ic-updater HTTP|
|28493|ic-updater cmd|
