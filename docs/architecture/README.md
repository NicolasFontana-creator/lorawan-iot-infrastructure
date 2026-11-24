# Arquitectura y evidencia

[Español](README.md) · [English](README.en.md)

![Nueve nodos LoRaWAN → Gateway A → TTN → MQTT → Node-RED. Node-RED alimenta FlowFuse, genera reportes PDF y escribe en InfluxDB. Grafana consulta las series y RStudio accede a los datos almacenados.](../../assets/diagrams/arquitectura-es.svg)

Los nueve nodos LoRaWAN del laboratorio se comunican con el Gateway A y están gestionados mediante The Things Network (TTN). Sobre esa infraestructura preexistente, Nicolás Nahuel Fontana desarrolló la plataforma que recibe las lecturas de TTN mediante MQTT, las procesa, las almacena y permite visualizarlas y generar reportes.

Node-RED escribe las lecturas en InfluxDB. Grafana consulta esas series para sus paneles. RStudio tiene acceso a los datos mediante la conexión configurada por el autor.

La referencia gráfica identifica placas SODAQ. Un ejemplo de reporte contiene esa denominación (p. 10); el nombre por sí solo no identifica el modelo ni el sensor empleado. En el esquema de referencia, LoRa describe la capa física de radio y LoRaWAN la arquitectura de acceso. El gateway enlaza la recepción radioeléctrica con el servidor de red. MQTT aparece después de esa etapa como interfaz de mensajería.

El cliente utiliza las interfaces de FlowFuse y Grafana. Los bloques representan funciones lógicas; el informe no especifica en qué máquinas se ejecutan ni documenta el dispositivo cliente de cada ensayo.

Fuente: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Laboratorio de Telecomunicaciones, UTN FR Paraná.
