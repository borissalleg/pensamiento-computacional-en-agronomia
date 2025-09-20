# 📚 **Introducción a Arduino en Ingeniería Agrícola**

> _“Automatiza el campo con tecnología accesible, eficiente y programable.”_

🌐 **Sitio Oficial de Arduino**: [https://www.arduino.cc](https://www.arduino.cc)

---

## 🤖 **1. ¿Qué es Arduino?**

**Arduino** es una plataforma de **hardware y software de código abierto**, diseñada para que personas sin experiencia previa en electrónica o programación puedan crear dispositivos que interactúen con el entorno físico.


![Arduino UNO](https://upload.wikimedia.org/wikipedia/commons/3/38/Arduino_Uno_-_R3.jpg)

*Figura 1: Arduino Uno R3 — La placa más usada para principiantes.*  
> Fuente: [Arduino Official Store](https://store.arduino.cc/products/arduino-uno-rev3)

- Ideal para **prototipado rápido**, educación, investigación y soluciones reales en el campo.
- Cuenta con una **comunidad global** que comparte librerías, códigos y proyectos.

---

## 🛠️ **2. ¿Para qué sirve Arduino?**

Arduino permite:

- **Leer datos** de sensores (temperatura, humedad, luz, pH, etc.).
- **Controlar actuadores** (motores, bombas, válvulas, relés, LEDs).
- **Tomar decisiones automáticas** basadas en condiciones programadas.
- **Comunicarse** con otros dispositivos (WiFi, Bluetooth, SD, pantallas, etc.).
- **Registrar y almacenar datos** para análisis posterior.

> ✅ En resumen: **Convierte tus ideas agrícolas en sistemas inteligentes y autónomos.**

---

## 🔧 3. Componentes principales de una placa Arduino (Ej: Arduino Uno)

![Diagrama de pines Arduino Uno](https://th.bing.com/th/id/R.835f9523017182461ca4efc6b48fc414?rik=KlMO%2by4GJjWAnQ&riu=http%3a%2f%2f3.bp.blogspot.com%2f-Rt8U1UsCUoU%2fVmsUCzB4njI%2fAAAAAAAAAes%2fT9fTSWWPjPA%2fs1600%2fPinout.jpg&ehk=NvmxTqficCwujmdB0rnRsr%2bdUc8kOSRnL9ibkMf%2fhSk%3d&risl=&pid=ImgRaw&r=0)  
*Figura 2: Distribución de pines en Arduino Uno R3.*  
> Fuente: [Documentación oficial de Arduino](https://docs.arduino.cc/hardware/uno-rev3)

| Componente               | Función                                                                 |
|--------------------------|-------------------------------------------------------------------------|
| **Microcontrolador**     | ATmega328P — El cerebro que ejecuta tu programa.                       |
| **Pines digitales/análogos** | Entradas y salidas para conectar sensores y actuadores.              |
| **Puerto USB**           | Conexión con la PC para programación y alimentación.                   |
| **Regulador de voltaje** | Estabiliza la energía para evitar daños.                               |
| **Botón de Reset**       | Reinicia el programa cargado.                                          |
| **LEDs integrados**      | Indican alimentación (ON) y actividad de transmisión (L, TX, RX).      |

> 💡 Puedes expandir sus capacidades con **shields** (placas de expansión) y módulos externos.

---

## 🌾 4. Aplicaciones en Ingeniería Agrícola

### 4.1. Riego Automático Inteligente



**Ejemplo básico:** activar bomba si la humedad es baja


![Montaje de prototipo](https://europe1.discourse-cdn.com/arduino/optimized/4X/9/1/4/9149425340de99e0969cf54245ad23440b4fa909_2_1380x906.png)


*Figura 3: Montaje de prototipo en placa Arduino Uno R3*  

Codigo fuente del proyecto en Arduino
    
    ```cpp

    int sensorHumedad = A0;
    int releBomba = 8;
    int valorHumedad;

    void setup() {
    pinMode(releBomba, OUTPUT);
    Serial.begin(9600);
    }

    void loop() {
    valorHumedad = analogRead(sensorHumedad);
    Serial.print("Humedad: ");
    Serial.println(valorHumedad);

    if (valorHumedad < 400) {  // Umbral ajustable
        digitalWrite(releBomba, HIGH);  // Enciende bomba
        delay(5000);                   // Riega 5 segundos
        digitalWrite(releBomba, LOW);   // Apaga bomba
    }
    delay(10000); // Espera 10 segundos antes de volver a medir
    }


## 🧰 Componentes Recomendados para Proyectos Agrícolas con Arduino

A continuación, se presenta una tabla con los componentes más utilizados en proyectos de automatización agrícola, junto con su imagen, descripción y función.

| Imagen | Componente | Descripción | Función en Proyectos Agrícolas |
|--------|------------|-------------|-------------------------------|
| ![Sensor de Humedad de Suelo](https://www.dbuelectronics.cr/4546-large_default/sensor-de-humedad-de-suelo.jpg) | **Sensor de Humedad de Suelo** | Mide el contenido de agua en el suelo mediante resistividad. Suele entregar una señal analógica o digital. | Permite activar riego automático cuando el suelo está seco. Ideal para agricultura de precisión. |
| ![Sensor de Lluvia](https://th.bing.com/th/id/OIP.Mdw0ybpfxAWAAvXisLLA7AHaHa?w=163&h=180&c=7&r=0&o=7&dpr=1.9&pid=1.7&rm=3) | **Sensor de Lluvia** | Detecta la presencia de agua sobre su superficie mediante placas conductoras. | Útil para suspender riego automático cuando llueve, ahorrando agua y energía. |
| ![Bomba de Agua Sumergible](https://http2.mlstatic.com/mini-bomba-de-agua-sumergible-120lh-arduino-D_NQ_NP_762145-MLC31211392372_062019-F.jpg) | **Bomba de Agua Sumergible (120L/h)** | Pequeña bomba de 5V-12V compatible con Arduino mediante relé. Ideal para prototipos. | Actuador principal en sistemas de riego automático. Se activa según lecturas de sensores. |
| ![Sensor de Temperatura y Humedad DHT11/DHT22](https://www.garizin.com/wp-content/uploads/2022/11/jpg-1-6.jpg) | **Sensor de Temperatura y Humedad (DHT11/DHT22)** | Mide temperatura ambiente y humedad relativa. Comunicación digital por 1 solo pin. | Monitoreo climático en invernaderos, establos o estaciones meteorológicas caseras. |
| ![Protoboard](https://1.bp.blogspot.com/-xTczv2OrB5w/X6cDy7H4KPI/AAAAAAAGOO4/VmfhaOwDs8wGdJyLiJ5826wt-2Lj5pqcwCLcBGAsYHQ/s1130/protoboard_01.png) | **Protoboard (Breadboard)** | Tabla de pruebas sin soldadura para armar circuitos temporales. | Permite conectar sensores, actuadores y Arduino sin dañar componentes. Ideal para prototipado rápido. |
| ![Cables para Protoboard](https://naylampmechatronics.com/785-medium_default_2x/cable-para-protoboard.jpg) | **Cables Jumper (Macho-Macho, Macho-Hembra)** | Cables con conectores en ambos extremos para unir componentes en la protoboard o con Arduino. | Facilitan las conexiones eléctricas entre sensores, actuadores y la placa Arduino. |

> 💡 **Nota**: Todas las imágenes son ilustrativas y pueden variar según el fabricante. Se recomienda verificar compatibilidad de voltaje y tipo de señal (digital/análoga) antes de comprar.

