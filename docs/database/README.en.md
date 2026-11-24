# Time series

[Español](README.md) · [English](README.en.md)

InfluxDB stores observations by board and time. Figure 12 (p. 13) shows its data explorer. The dashboard requests statistics once a minute (pp. 6–7) and supports manual time-range queries. Grafana uses the database for its panels (pp. 14–15). The map demonstrates use of location data; how those locations were obtained is unspecified.

Node-RED writes samples to InfluxDB. RStudio accesses the series through the connection confirmed by the author.

The report describes Flux and InfluxQL as query options. Original queries, installed version, retention policy and downsampling configuration were unavailable.

Source: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Telecommunications Laboratory, UTN FR Paraná.
