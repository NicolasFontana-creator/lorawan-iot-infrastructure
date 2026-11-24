# Journey of a reading

[Español](README.md) · [English](README.en.md)

Node.js provides the backend runtime. Node-RED receives MQTT events from TTN, writes readings to InfluxDB and updates FlowFuse Dashboard. An incoming event updates the corresponding sensor card. Independently, the dashboard queries InfluxDB once a minute for statistics.

In figure 7 (p. 9), each timestamp has temperature, RSSI, SNR, latitude and longitude fields. Figures 5–7 query one board over the last ten minutes. This example window differs from the periodic indicator query. The report supplies neither a raw MQTT message nor an exported flow for checking the decoder.

Source: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Telecommunications Laboratory, UTN FR Paraná.
