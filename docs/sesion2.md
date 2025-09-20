# 🧩 SESIÓN 2: Descomposición de Problemas Agronómicos

> *"¿Te abruma un problema grande? No te preocupes. Hoy aprenderás a cortarlo en pedacitos… ¡y cada pedacito será fácil de resolver!"*

---

## 🎯 Objetivos de la Sesión

Al finalizar esta sesión, el estudiante será capaz de:

1.  **Aplicar la técnica de descomposición** para dividir un problema agronómico complejo en subproblemas más pequeños, simples y manejables.
2.  **Identificar los componentes clave** de un sistema agrícola (sensores, actuadores, variables ambientales) que podrían ser simulados en Tinkercad.
3.  **Crear un diagrama de flujo de alto nivel** que represente la lógica de solución de su problema de proyecto.
4.  **Comenzar a pensar en términos de “entradas, procesos y salidas”** como base para futuros algoritmos y simulaciones.

---

## 🧠 Conceptos Clave (Explicados sin tecnicismos)

### ¿Qué es la Descomposición?

> Imagina que tienes que comer una pizza entera. ¿Te la metes toda a la boca? ¡No! La partes en porciones. **Descomponer** es eso: tomar un problema GRANDE y partirlo en porciones pequeñas que puedes manejar una por una.

En ingeniería agronómica, esto es VITAL. Porque los problemas del campo rara vez tienen una sola causa.

---

### ¿Cómo se Descompone un Problema Agrícola?

Sigue estos pasos sencillos:

1.  **Define el problema principal** con claridad.
    *   ❌ Mal: “Mi cultivo no va bien.”
    *   ✅ Bien: “El rendimiento del maíz en la parcela A disminuyó un 30% este año.”

2.  **Hazte preguntas clave:**
    *   ¿Qué factores podrían estar influyendo? (Clima, suelo, plagas, riego, semilla, manejo).
    *   ¿Qué datos necesito para investigar cada factor?
    *   ¿Qué parte del problema puedo resolver primero?

3.  **Crea una “lista de chequeo” de subproblemas.**
    *   Subproblema 1: Analizar datos de precipitación del último año.
    *   Subproblema 2: Revisar el análisis de suelo de la parcela A.
    *   Subproblema 3: Verificar si hubo presencia de plagas en la etapa crítica.

---

### 💡 Ejemplo Real: “Las plantas de tomate se están marchitando”

**Problema Principal:** Marchitez generalizada en invernadero.

**Descomposición:**

| Subproblema | ¿Qué necesito investigar? | ¿Qué herramienta podría usar? |
| :---------- | :------------------------ | :---------------------------- |
| **1. Riego** | ¿Está el sistema funcionando? ¿Frecuencia y volumen son adecuados? | Sensor de humedad (Tinkercad) + registro de riegos. |
| **2. Suelo** | ¿pH y nutrientes están en rango? | Análisis de laboratorio + comparar con tablas agronómicas. |
| **3. Plagas/Enfermedades** | ¿Hay hongos en raíces o tallos? | Inspección visual + microscopio. |
| **4. Clima (invernadero)** | ¿Temperatura y humedad del aire están controladas? | Sensor DHT11 (Tinkercad) + registro de datos. |

👉 *Al descomponerlo, ves que no es un solo problema, ¡son 4! Y puedes asignar a cada miembro del equipo un subproblema.*

---

## 🛠 Actividades de la Sesión (Manos a la Obra)

### Actividad 1: Taller Práctico — “Cortando el Problema en Pedazos”

*   **Instrucciones:**
    1.  En equipos, retomen el **problema agrícola** que eligieron en la Sesión 1.
    2.  Aplicando la técnica aprendida, **descompongan ese problema en al menos 3-5 subproblemas**.
    3.  Para cada subproblema, identifiquen:
        *   ¿Qué datos necesitan?
        *   ¿Qué herramienta o método usarían para resolverlo? (¿Sensor? ¿Análisis de suelo? ¿Encuesta? ¿Simulación en Tinkercad?).
    4.  Presenten su descomposición en una hoja de rotafolio o en una diapositiva simple.

*   **Duración:** 40 minutos.
*   **Entregable:** Una lista clara de subproblemas con sus respectivos “qué necesito” y “cómo lo resuelvo”.

---

### Actividad 2: Diagrama de Flujo + Primer Acercamiento a Tinkercad (Parte 2)

*   **Paso 1: Crea un Diagrama de Flujo Simple**
    *   Con base en su descomposición, el equipo debe dibujar un **diagrama de flujo de ALTO NIVEL** que muestre los pasos lógicos para abordar el problema.
    *   Ejemplo simple:
        ```
        [Inicio] → [¿Está seco el suelo?] → (Sí) → [Activar riego] → [Fin]
                                   ↓
                                  (No) → [Esperar 1 hora] → [Volver a medir]
        ```

*   **Paso 2: Conecta tu Diagrama con Tinkercad**
    *   El docente guiará a los equipos para que identifiquen:
        *   ¿Qué partes de su diagrama de flujo podrían **simularse con sensores y actuadores en Tinkercad**?
        *   Ejemplo: Si su diagrama dice “Si está seco, regar”, entonces necesitan un **sensor de humedad** y una **bomba (actuador)** en la simulación.
    *   **Tarea grupal:** Hagan una lista de los componentes electrónicos que necesitarían en Tinkercad para simular su solución.

> 💬 *"No tienen que construirlo todavía. Solo imaginarlo. Hoy están diseñando el ‘esqueleto’ de su solución. La ‘carne’ (el código y la simulación) viene después."*

---

## 📌 Para Llevar (Takeaways)

✅ **Descomponer = Dividir para vencer.** Es la primera herramienta para no ahogarte en problemas complejos.
✅ Todo problema agronómico se puede partir. ¡Empieza por hacer las preguntas correctas!
✅ Tu **diagrama de flujo** es el mapa del tesoro de tu solución.
✅ **Tinkercad** es donde ese mapa se convierte en algo que puedes ver y probar.

---

## 📚 Tarea / Trabajo Independiente

1.  **Refina tu descomposición:** Toma el trabajo de tu equipo y mejóralo individualmente. Añade al menos UN subproblema más o profundiza en uno existente.
2.  **Dibuja tu diagrama de flujo personal:** Haz una versión más detallada o más clara de lo que hizo el equipo. Puedes usar herramientas como:
    *   [draw.io](https://app.diagrams.net/) (gratis y fácil)
    *   PowerPoint
    *   ¡Una hoja y un lápiz!
3.  **Explora Tinkercad (Parte 1):**
    *   Ingresa a [Tinkercad.com](https://www.tinkercad.com/) y ve a la sección “Circuits”.
    *   Busca y arrastra al área de trabajo los siguientes componentes (solo para familiarizarte):
        *   `Arduino Uno`
        *   `Moisture Sensor` (Sensor de humedad)
        *   `Water Pump` (Bomba de agua)
        *   `LED`
    *   **NO tienes que conectarlos ni programarlos aún.** Solo identifícalos y juega un poco moviéndolos.

---

## 💬 Mensaje Final del Instructor

> “La grandeza no está en resolver problemas gigantes de un solo golpe. Está en tener la sabiduría para partirlos, la paciencia para resolverlos uno a uno, y la visión para ver cómo todas las piezas encajan. Hoy no solo aprendiste una técnica, aprendiste una filosofía para enfrentar cualquier desafío en tu carrera. ¡Y lo mejor es que ya empezaron a aplicarla!” 🧩🚜

**Sigan cortando problemas… ¡y convirtiéndolos en soluciones!**