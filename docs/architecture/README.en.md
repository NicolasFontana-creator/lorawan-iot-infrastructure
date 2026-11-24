# Architecture and evidence

[Español](README.md) · [English](README.en.md)

![Nine LoRaWAN nodes → Gateway A → TTN → MQTT → Node-RED. Node-RED updates FlowFuse, generates PDF reports and writes to InfluxDB. Grafana queries the time series and RStudio accesses stored data.](../../assets/diagrams/architecture-en.svg)

The laboratory’s nine LoRaWAN nodes communicate with Gateway A and are managed through The Things Network (TTN). Nicolás Nahuel Fontana developed the software platform that receives readings from TTN over MQTT, processes and stores them, and supports visualization and reporting.

Node-RED writes readings to InfluxDB. Grafana queries the stored series for its panels. RStudio can access the data through the connection configured by the author.

The reference identifies SODAQ boards; an example report includes that name (p. 10). It does not establish a board or sensor model. LoRa denotes the radio physical layer and LoRaWAN the access architecture. The gateway connects radio reception with the network server. MQTT is the downstream messaging interface.

Users access FlowFuse and Grafana in a browser. Blocks denote logical functions. The host allocation and the individual client devices used in tests are unspecified.

Source: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Telecommunications Laboratory, UTN FR Paraná.
