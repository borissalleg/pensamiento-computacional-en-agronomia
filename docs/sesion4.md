# 🎨 SESIÓN 4: Abstracción y Modelado de Sistemas Agrícolas

> *"No necesitas entender TODO para resolver algo. Solo lo esencial. Hoy aprenderás a filtrar el ruido… y quedarte con lo que realmente importa."*

---

## 🎯 Objetivos de la Sesión

Al finalizar esta sesión, el estudiante será capaz de:

1.  **Definir la abstracción** como componente clave del pensamiento computacional.
2.  **Aplicar técnicas de abstracción** para simplificar sistemas agrícolas complejos (como un invernadero, un sistema de riego o un ciclo de cultivo).
3.  **Crear un modelo abstracto** (diagrama o pseudocódigo) que represente solo las variables y relaciones relevantes para resolver un problema específico.
4.  **Traducir ese modelo a un esquema de circuito básico en Tinkercad**, identificando sensores y actuadores esenciales.

---

## 🧠 Conceptos Clave (Explicados sin tecnicismos)

### ¿Qué es la Abstracción?

> Es como usar un **mapa del tesoro**: no muestra cada hoja, cada piedra ni cada hormiga del camino. Solo muestra lo que necesitas para llegar al cofre.  
> **Abstraer = Eliminar lo innecesario y quedarte con lo esencial para resolver tu problema.**

En agronomía, esto es vital. Porque si intentas modelar **todo** de un cultivo (desde la raíz hasta el clima global), ¡nunca terminarás!

---

### ¿Por qué la Abstracción NO es “ignorar”?

*   **Ignorar** = No saber qué variables importan.
*   **Abstraer** = Saber **exactamente** qué variables son relevantes **para tu objetivo específico**.

#### Ejemplo: Sistema de Riego Automático

| ¿Quieres...? | Variables ESENCIALES (abstracción útil) | Variables que puedes IGNORAR |
| :----------- | :-------------------------------------- | :--------------------------- |
| **Optimizar agua** | Humedad del suelo, tipo de suelo, etapa del cultivo, evapotranspiración | Color de la flor, nombre del agricultor, marca de la semilla |
| **Prevenir plagas** | Temperatura, humedad del aire, presencia de insectos | pH del suelo, velocidad del viento, hora del día |

👉 *La abstracción depende de TU OBJETIVO.*

---

### 💡 Caso Real: Modelando un Invernadero Inteligente

**Problema:** “Quiero mantener la temperatura ideal para lechugas (18–22°C) sin gastar energía de más.”

**Abstracción inteligente:**
- **Solo me importa:** Temperatura dentro del invernadero.
- **No me importa (por ahora):** Humedad, luz, CO₂, tipo de sustrato, etc.
- **Acciones posibles:** Encender ventilador si >22°C, encender calefacción si <18°C.

**Modelo abstracto en pseudocódigo:**

    INICIO
        LEER temperatura_interna
        SI temperatura_interna > 22°C ENTONCES
            ENCENDER ventilador
        SINO SI temperatura_interna < 18°C ENTONCES
            ENCENDER calefacción
        SINO
            APAGAR todos los dispositivos
        FIN SI
    FIN

### Actividad 1: Taller — “¿Qué SÍ y qué NO necesito?”

*   **Instrucciones:**
    1.  En equipos, retomen el **problema agrícola** de su proyecto.
    2.  Definan **UN objetivo claro y específico** (ej: “Reducir el uso de agua en riego”).
    3.  Hagan dos columnas:
        *   **Columna A: Variables ESENCIALES** (las que afectan directamente su objetivo).
        *   **Columna B: Variables que puedo ABSTRAER (ignorar por ahora)**.
    4.  Justifiquen por qué cada variable está en su columna.

*   **Duración:** 25 minutos.  
*   **Entregable:** Una tabla clara con las dos columnas y sus justificaciones.

---

### Actividad 2: Crea tu Modelo Abstracto

*   **Instrucciones:**
    1.  Con base en su abstracción, el equipo debe crear **UN modelo simple** que represente su solución. Puede ser:
        *   Un **diagrama de bloques** (cajas y flechas).
        *   Un **pseudocódigo** (como el del invernadero).
        *   Un **dibujo esquemático** del sistema.
    2.  El modelo debe incluir:
        *   **Entradas** (qué datos necesita: ej. humedad, temperatura).
        *   **Proceso** (qué decisión toma: ej. si X, entonces Y).
        *   **Salidas** (qué acción realiza: ej. encender bomba, enviar alerta).

*   **Duración:** 20 minutos.  
*   **Entregable:** El modelo en papel o digital.

---

### Actividad 3: Diseña tu Circuito en Tinkercad (¡Solo el Esquema!)

*   **Paso 1: Traduce tu modelo a componentes**  
    El docente guiará la identificación de:
    *   ¿Qué sensor representa tu **entrada**? (ej: `Moisture Sensor` para humedad).
    *   ¿Qué actuador representa tu **salida**? (ej: `Water Pump` o `LED`).
    *   ¿Qué “cerebro” lo controla? (`Arduino Uno`).

*   **Paso 2: Arma el esquema (sin programar aún)**  
    *   En Tinkercad → “Circuits” → “Create new Circuit”.
    *   Arrastren los componentes que identificaron.
    *   **Conéctenlos con cables** (solo para ver cómo se vería físicamente).
    *   **NO programen todavía.** Solo armen el esqueleto.

---

> 💬 **Reflexión grupal:**  
> *“¿Ves cómo tu modelo abstracto… se convierte en un circuito real (aunque sea virtual)? Eso es ingeniería: pasar de la idea al diseño.”*