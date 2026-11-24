# Infraestructura IoT LoRaWAN

[Español](README.md) · [English](README.en.md)

**Nicolás Nahuel Fontana · Laboratorio de Telecomunicaciones, UTN Facultad Regional Paraná.**

Para estudiar la gestión de recursos en ciudades inteligentes, el laboratorio reunió en una plataforma las lecturas de nueve placas, la calidad de señal y la posición de los dispositivos. El operador puede observar una actualización, recuperar el historial y conservar una observación en un reporte.

![Ruta conceptual de nodos al gateway y TTN; integración documentada de MQTT con Node-RED, InfluxDB, FlowFuse, reportes PDF y Grafana.](assets/diagrams/arquitectura-es.svg)

Las flechas discontinuas identifican el acceso propuesto en la referencia conceptual. El informe muestra nueve placas y la recepción de eventos MQTT. El modelo del gateway, el enlace de retorno y el alta en The Things Network (TTN) quedan pendientes de evidencia de configuración.

## Procesamiento y almacenamiento

Node.js proporciona el entorno de ejecución del backend. Node-RED integra los eventos MQTT con el dashboard FlowFuse y las series de InfluxDB. Una llegada MQTT actualiza la tarjeta del sensor correspondiente; las estadísticas se consultan por separado, cada minuto.

## Dashboards y consultas

FlowFuse muestra la última temperatura por placa y los estados Frío, Normal y Calor. Los indicadores incluyen promedio, extremos y dispersión de temperatura, RSSI en dBm y SNR en dB. El formulario histórico permite elegir placa y período. Grafana consulta InfluxDB para mostrar temperaturas, ubicación e indicadores de radio.

## Reportes por dispositivo

Desde el dashboard, el operador selecciona dispositivo y aplicación, escribe observaciones y guarda el reporte. La plataforma conserva el PDF en un directorio con el dispositivo y la marca temporal en el nombre.

## Resultados y próximos pasos

El informe confirma la interconexión funcional de las herramientas. Las capturas registran el estado del ensayo. No se publicaron mediciones de latencia, disponibilidad o consumo. RStudio, el análisis predictivo y la ampliación de la gestión de volúmenes de datos aparecen como trabajo futuro.

## Documentación

- [Arquitectura y evidencia](docs/architecture/README.md)
- [Recorrido de una lectura](docs/data-flow/README.md)
- [Backend y reportes](docs/backend/README.md)
- [Series temporales](docs/database/README.md)
- [Galería y consultas](docs/dashboards/README.md)
- [Resultados y alcance](docs/results/README.md)
