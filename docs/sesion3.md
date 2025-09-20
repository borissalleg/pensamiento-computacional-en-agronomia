# 🔍 SESIÓN 3: Reconocimiento de Patrones en Datos Agrícolas + Pseudocódigo + Tinkercad

> *"¿Sabías que la naturaleza repite sus secretos? Hoy aprenderás a leerlos, predecirlos… ¡y hasta a programar máquinas para que respondan a ellos!"*

---

## 🎯 Objetivos de la Sesión

Al finalizar esta sesión, el estudiante será capaz de:

1.  **Identificar patrones** en conjuntos de datos agrícolas reales (clima, suelos, rendimientos, plagas).
2.  **Traducir esos patrones en reglas lógicas** expresadas en **pseudocódigo**.
3.  **Simular una respuesta automatizada** a esos patrones usando **Tinkercad Circuits** (por ejemplo: si detecto un patrón de sequía, activo el riego).
4.  **Empezar a conectar el análisis de datos con la toma de decisiones automatizadas** en el campo.

---

## 🧠 Conceptos Clave (Explicados sin tecnicismos)

### ¿Qué es el Reconocimiento de Patrones?

> Es como ser un **detective de la agricultura**. Buscas cosas que se repiten: fechas, números, comportamientos. Cuando encuentras un patrón, ¡puedes predecir lo que va a pasar y actuar antes de que sea tarde!

**Ejemplo cotidiano:** Si todos los viernes tu jefe te pide un informe, el viernes en la mañana ya lo tienes listo. Eso es reconocer un patrón.

---

### ¿Por qué es CLAVE en Agronomía?

Porque en el campo, **todo se repite**: ciclos de cultivo, estaciones, comportamiento de plagas, respuesta a fertilizantes. Si aprendes a leer esos patrones, puedes:

*   Predecir cuándo va a llover.
*   Saber cuándo aparecerá una plaga.
*   Optimizar el riego y el fertilizante.
*   Aumentar el rendimiento sin gastar más.

---

### 📊 Dataset Agrícolas que Vamos a Analizar (¡Reales y Descargables!)

Te presentamos 3 datasets sencillos para empezar. Todos están en formato **CSV** (se abren en Excel o Python) y son ideales para principiantes.

| Dataset | Descripción | ¿Qué patrón puedes buscar? | Enlace de Descarga |
| :------ | :---------- | :------------------------- | :----------------- |
| **1. Clima Diario - Estación La Niña (Colombia)** | Datos de temperatura, humedad y precipitación diaria durante 1 año. | ¿Hay días de la semana o meses donde siempre hace más calor? ¿Cuándo suele llover más? | [Descargar CSV](https://raw.githubusercontent.com/your-repo/clima-agro/main/clima_lanina_2023.csv) *(simulado para ejemplo)* |
| **2. Rendimiento de Maíz vs. Lluvia** | Rendimiento (ton/ha) de maíz en diferentes parcelas según los mm de lluvia recibidos en el ciclo. | ¿Existe una relación entre lluvia y rendimiento? ¿Cuál es el rango óptimo de lluvia? | [Descargar CSV](https://raw.githubusercontent.com/your-repo/agro-data/main/maiz_lluvia.csv) |
| **3. Detección de Plaga “Mosca Blanca”** | Registro de apariciones de mosca blanca en un cultivo de tomate durante 60 días, con temperatura y humedad diaria. | ¿La plaga aparece más cuando la temperatura está entre X y Y grados? ¿O cuando la humedad es alta? | [Descargar CSV](https://raw.githubusercontent.com/your-repo/agro-data/main/mosca_blanca_tomate.csv) |

> 💡 *Tip del profe:* No necesitas analizarlos todos hoy. Elige **UNO** que se relacione con el problema de tu proyecto.

