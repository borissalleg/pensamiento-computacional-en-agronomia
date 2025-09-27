# 💻 SESIÓN 6: Introducción a Python para Ingenieros Agrónomos

> *"Hoy no aprenderás a ser un programador. Aprenderás a usar Python como una herramienta para hacer tu trabajo en el campo más inteligente, más rápido y más preciso."*

---

## 🎯 Objetivos de la Sesión

Al finalizar esta sesión, el estudiante será capaz de:

1.  **Instalar y configurar** un entorno básico de Python (Jupyter Notebook o Google Colab).
2.  **Reconocer y usar** los elementos básicos del lenguaje: variables, tipos de datos, operadores y funciones de entrada/salida (`print`, `input`).
3.  **Escribir scripts simples en Python** que realicen cálculos agronómicos (ej: dosis de fertilizante, eficiencia de riego).
4.  **Relacionar la lógica aprendida en pseudocódigo y Tinkercad** con la sintaxis real de Python.

---

## 🧠 Conceptos Clave (Explicados sin tecnicismos)

### ¿Por qué Python?

> Python es como el **“español del mundo de la programación”**: es sencillo de leer, potente y usado en ciencia, agricultura, finanzas, inteligencia artificial… ¡y hasta en la NASA!  
> Para ti, como ingeniero agrónomo, es la llave para **analizar datos, automatizar reportes y tomar decisiones basadas en evidencia**.

---

### Elementos Básicos de Python

| Concepto | ¿Qué es? | Ejemplo Agronómico |
| :------- | :------- | :----------------- |
| **Variable** | Un “cajón con nombre” donde guardas un valor. | `humedad = 45` → Guardo el valor 45 en la variable `humedad`. |
| **Tipo de dato** | El “tipo de cosa” que guarda la variable. | `45` → número entero (`int`)<br>`"maíz"` → texto (`str`)<br>`23.5` → número decimal (`float`) |
| **Operadores** | Símbolos para hacer cálculos. | `+`, `-`, `*`, `/`, `**` (potencia) |
| **`print()`** | Muestra algo en la pantalla. | `print("La humedad es:", humedad)` |
| **`input()`** | Pide al usuario que escriba algo. | `cultivo = input("¿Qué cultivo estás manejando? ")` |

---

### 💡 Ejemplo 1: Cálculo de Dosis de Fertilizante

```python

    # Datos del agricultor
    area_hectareas = 2.5
    dosis_kg_por_hectarea = 120

    # Cálculo
    fertilizante_total = area_hectareas * dosis_kg_por_hectarea

    # Resultado
    print("Debes aplicar", fertilizante_total, "kg de fertilizante en total.")

### Actividad 1: Configuración del Entorno

*   **Instrucciones:**
    1.  Accede a [Google Colab](https://colab.research.google.com/) (¡no requiere instalación!).
    2.  Crea un nuevo cuaderno (“Notebook”).
    3.  Escribe y ejecuta tu primer código:
        ```python
        print("¡Hola, futuro ingeniero agrónomo!")
        ```
    4.  Experimenta: cambia el mensaje y vuelve a ejecutar.

*   **Duración:** 15 minutos.  
*   **Entregable:** Captura de pantalla de tu primer `print()` funcionando.

---

### Actividad 2: Script de Cálculo Agronómico

*   **Instrucciones:**
    1.  En equipos, elijan **UN cálculo agronómico** que usen frecuentemente:
        *   Dosis de semilla por hectárea.
        *   Rendimiento en ton/ha.
        *   Volumen de agua para riego.
        *   Porcentaje de germinación.
    2.  Escriban un script en Python que:
        *   Use variables con nombres claros.
        *   Realice el cálculo.
        *   Muestre el resultado con `print()`.
    3.  **Ejemplo de estructura:**
        ```python
        # Mi script: Cálculo de rendimiento
        peso_cosecha_kg = 12500
        area_hectareas = 2.0
        rendimiento = peso_cosecha_kg / area_hectareas / 1000  # a ton/ha
        print("Rendimiento:", rendimiento, "ton/ha")
        ```

*   **Duración:** 30 minutos.  
*   **Entregable:** Script funcional en Google Colab (compartir enlace o captura).

---

### Actividad 3: Conexión con lo Aprendido

*   **Instrucciones:**
    1.  Retomen el **pseudocódigo** que escribieron en la Sesión 5.
    2.  Identifiquen:
        *   ¿Qué variables usarían en Python?
        *   ¿Cómo se vería la condición `SI...ENTONCES` en Python? (`if...:`)
    3.  Escriban **solo la primera línea** de una condición en Python:
        ```python
        if humedad_suelo < 30:
            print("¡Activar riego!")
        ```

*   **Duración:** 15 minutos.  
*   **Entregable:** Comparación escrita: pseudocódigo vs. sintaxis Python.

---

> 💬 **Reflexión grupal:**  
> *“Lo que antes escribías en palabras, ahora lo escribes en un lenguaje que la computadora entiende. No estás aprendiendo a programar por programar. Estás aprendiendo a darle órdenes precisas a una herramienta que multiplicará tu impacto en el campo.”*

ESQUEMA DE ANÁLISIS DE LOGS – IUD GPT  
Proyecto: Validación e implementación del asistente virtual IUD GPT  

**Objetivo:**  
Analizar el uso, rendimiento y eficiencia técnica del asistente virtual a partir de datos registrados automáticamente.  

**Fuente de datos:**  
Base de datos PostgreSQL del sistema IUD GPT (tablas de auditoría y registro de consultas).  

**Variables a recolectar:**  

| Variable | Descripción | Tipo de dato |
|--------|------------|-------------|
| ID_Usuario | Identificador anónimo del usuario | Numérico |
| Curso | Curso desde el que se accede a IUD GPT | Texto |
| Fecha y hora | Timestamp de la consulta | Fecha/hora |
| Tipo_consulta | Académica, técnica, administrativa, general | Categórico |
| Consulta | Texto de la pregunta realizada (anónimo) | Texto |
| Respuesta | Texto de la respuesta generada | Texto |
| Tiempo_respuesta | Tiempo en segundos desde la consulta hasta la respuesta | Numérico |
| Éxito | 1 = respuesta útil, 0 = no comprendida | Binario |
| Nivel_academico | Semestre del estudiante (si aplica) | Numérico |
| Modo_uso | Estudiante, docente | Categórico |

**Herramientas de análisis:**  
- **Python (Pandas, Matplotlib, Seaborn):** Para limpieza, visualización y estadística descriptiva.  
- **Power BI o Excel:** Para dashboards simples y gráficos.  
- **SPSS o R:** Para análisis inferencial (pruebas t, correlaciones).  

**Indicadores clave (KPIs):**  
1. Número total de consultas por semana.  
2. Distribución por tipo de consulta.  
3. Tiempo de respuesta promedio.  
4. Tasa de éxito (consultas resueltas vs. no comprendidas).  
5. Cursos con mayor interacción.  
6. Horario de mayor uso.  

**Reporte final:**  
Informe técnico con gráficos, tablas y hallazgos clave, integrado al artículo científico (ART-C).  