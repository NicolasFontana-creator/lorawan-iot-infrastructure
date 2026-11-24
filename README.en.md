# LoRaWAN IoT Infrastructure

[Español](README.md) · [English](README.en.md)

**Nicolás Nahuel Fontana · Telecommunications Laboratory, UTN Facultad Regional Paraná.**

To study resource management in smart cities, the laboratory brought readings from nine boards, signal quality and device locations into one platform. An operator can inspect an update, retrieve earlier samples and preserve an observation in a report.

![Conceptual sensor, gateway and TTN path; documented MQTT, Node-RED, InfluxDB, FlowFuse, PDF and Grafana integration.](assets/diagrams/architecture-en.svg)

Dashed arrows identify the access path in the conceptual reference. The report shows nine boards and incoming MQTT events. Gateway model, backhaul and registration with The Things Network (TTN) still require configuration evidence.

## Processing and storage

Node.js provides the backend runtime. Node-RED connects MQTT events with FlowFuse Dashboard and InfluxDB time series. An incoming event updates the corresponding sensor card. Independently, the dashboard queries stored readings once a minute for statistics.

## Dashboards and queries

FlowFuse shows the latest temperature per board and the Cold, Normal and Hot states. Indicators include mean, extremes and spread of temperature, RSSI in dBm and SNR in dB. Operators select a board and time range for historical queries. Grafana queries InfluxDB for temperature, location and radio panels.

## Device reports

From the dashboard, the operator selects a device and application, enters observations and saves the report. The platform keeps the PDF in a directory, with the device and timestamp in its filename.

## Results and future work

The report confirms functional integration of the software tools. Screenshots record the state of the trial. No latency, availability or energy measurements were reported. RStudio, predictive analysis and improved handling of large data volumes are future work.

## Documentation

- [Architecture and evidence](docs/architecture/README.en.md)
- [Journey of a reading](docs/data-flow/README.en.md)
- [Backend and reports](docs/backend/README.en.md)
- [Time series](docs/database/README.en.md)
- [Panels and queries](docs/dashboards/README.en.md)
- [Results and scope](docs/results/README.en.md)
