# Recorrido de una lectura

[Español](README.md) · [English](README.en.md)

Node.js proporciona el entorno de ejecución del backend. Node-RED recibe los eventos MQTT de TTN, escribe las lecturas en InfluxDB y actualiza FlowFuse Dashboard. Una llegada MQTT actualiza la tarjeta del sensor correspondiente; FlowFuse obtiene las estadísticas mediante consultas a InfluxDB cada minuto.

La tabla de la ilustración 7 (p. 9) asocia a una marca temporal los campos de temperatura, RSSI, SNR, latitud y longitud. La consulta de las ilustraciones 5–7 selecciona una placa en los últimos diez minutos. Esta ventana de ejemplo es distinta de la consulta periódica de indicadores. El documento no aporta un mensaje MQTT en bruto ni el flujo exportado que permitiría verificar el decodificador.

Fuente: Nicolás Nahuel Fontana, *Gestión eficiente de recursos en ciudades inteligentes. Desarrollo de una plataforma IoT*, Laboratorio de Telecomunicaciones, UTN FR Paraná.
