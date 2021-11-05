## Collecting :satellite:CSI:satellite: from the WiFi station

This code is build off from the ESP32 station example, which set a board as a station and connect it to the target access point.

To collect CSI (channel state information) from the station side, following steps need to be done:
1. Configure the device to station mode, and connect it to target access point
2. Call ESP wifi set csi APIs
3. Ping the access point from the station

### Which ESP wifi set csi APIs to use?
- [ ] Create a callback function for the *esp_wifi_set_csi_rx_cb* API and call the API with porper argument
- [ ] Create a struct (type: *wifi_csi_config_t*) to be passed in *esp_wifi_set_csi_config* which contains the configuration
- [ ] Call *esp_wifi_set_csi* API with argument _true_

### How to ping the access point
- [ ] Save the access point IP address into _gw.addr_
- [ ] Call *esp_ping_set_target* API
- [ ] Call ping_init()