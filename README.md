# PRACTICA-ESP32-con-DHT11
## INTRODUCCION 
### Descripcion 
La Esp32 es una tarjeta de adquisición de datos, paralo cual en esta practica ocuparemos un sensor (DTH11) para adquirir datos de temperatura y humedad del entorno cada segundo, se usara un simulador llamado WOKWI.
## MATERIAL A UTILIZAR
- [WOKWI](https://wokwi.com/projects/new/esp32)
- TARJET ESP32
- SENSOR DHT11
## INSTRUCCIONES
### Instrucciones de preparación de entorno 

1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}

```
2. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/Victor-Cabanas-99/PRACTICA-ESP32-con-DHT11/blob/main/DHT11%20LIBRERIA.PNG?raw=true)

3. Hacer la conexion de **DHT11** con la **ESP32** como se muestra en la siguente imagen.

![](https://github.com/Victor-Cabanas-99/PRACTICA-ESP32-con-DHT11/blob/main/DHT11%20RESULTADOS.PNG?raw=true)

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT11**

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.
![](https://github.com/Victor-Cabanas-99/PRACTICA-ESP32-con-DHT11/blob/main/DHT11%20RESULTADOS.PNG?raw=true)

### Desarrollado por 
VICTOR EMANUEL CABAÑAS MONTES

