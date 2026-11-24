# Series temporales

[Español](README.md) · [English](README.en.md)

InfluxDB conserva las observaciones por placa y tiempo. El explorador de datos aparece en la ilustración 12 (p. 13). El dashboard solicita estadísticas cada minuto (pp. 6–7) y admite consultas manuales por período. Grafana usa la base como fuente de sus paneles (pp. 14–15). La figura del mapa evidencia el uso de información geográfica, pero no establece si las posiciones fueron configuradas o adquiridas mediante GNSS.

Node-RED escribe las muestras en InfluxDB. RStudio accede a las series mediante la conexión confirmada por el autor.

El informe presenta Flux e InfluxQL como opciones de consulta. No adjunta sentencias originales, versión instalada, política efectiva de retención ni configuración de downsampling.

Fuente: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Laboratorio de Telecomunicaciones, UTN FR Paraná.
