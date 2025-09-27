# 📝 SESIÓN 5: Fundamentos de Algoritmos y Lógica — Del Pseudocódigo a los Bloques en Tinkercad

> *"Un algoritmo no es magia. Es una receta clara, paso a paso, para que una máquina (o tú) resuelva un problema. Hoy aprenderás a escribirla… ¡y a hacer que una simulación la ejecute!"*

---

## 🎯 Objetivos de la Sesión

Al finalizar esta sesión, el estudiante será capaz de:

1.  **Definir qué es un algoritmo** y explicar su importancia en la automatización de tareas agrícolas.
2.  **Diseñar algoritmos en pseudocódigo** usando estructuras de control básicas: **condicionales (`SI...ENTONCES...SINO`)** y **bucles (`REPETIR MIENTRAS...`)**.
3.  **Traducir algoritmos desde pseudocódigo a bloques de programación visual** en **Tinkercad Circuits**.
4.  **Simular la ejecución de un algoritmo** que responda a condiciones del entorno agrícola (ej: activar riego si el suelo está seco).

---

## 🧠 Conceptos Clave (Explicados sin tecnicismos)

### ¿Qué es un Algoritmo?

> Es una **secuencia ordenada y sin ambigüedades de pasos** para resolver un problema o realizar una tarea.  
> **¡Ya los usas todos los días!**  
> Ejemplo: *“Para regar mis plantas: 1) Tomo la manguera, 2) Abro la llave, 3) Riego cada planta 10 segundos, 4) Cierro la llave.”* → ¡Eso es un algoritmo!

En ingeniería agronómica, los algoritmos permiten **automatizar decisiones** basadas en datos del campo.

---

### Estructuras de Control Básicas

#### 1. **Condicionales (`SI...ENTONCES...SINO`)**
> Permiten que el sistema **tome decisiones** según una condición.

**Ejemplo agrícola en pseudocódigo:**

    SI humedad_suelo < 30% ENTONCES
        activar_bomba()
    SINO
        mantener_bomba_apagada()
    FIN SI

### 🌾 Más Ejemplos de Condicionales en Contextos Agrícolas

Los condicionales (`SI...ENTONCES...SINO`) son la base de la toma de decisiones automatizada. Aquí tienes ejemplos prácticos que puedes usar como inspiración para tu proyecto o simulaciones en Tinkercad.

---

#### Ejemplo 1: Riego Inteligente por Humedad y Etapa del Cultivo

    SI etapa_cultivo = "floración" Y humedad_suelo < 40% ENTONCES
        activar_riego(20 minutos)
    SINO SI etapa_cultivo = "llenado de grano" Y humedad_suelo < 30% ENTONCES
        activar_riego(15 minutos)
    SINO
        mantener_riego_apagado()
    FIN SI

#### Ejemplo 2: Alerta de Helada en Cultivos Sensibles

    SI temperatura_aire < 2°C Y tipo_cultivo = "fresa" ENTONCES
        activar_calefaccion()
        enviar_alerta("¡Riesgo de helada en fresas!")
    SINO SI temperatura_aire < 0°C Y tipo_cultivo = "papa" ENTONCES
        cubrir_cultivo()
    FIN SI

#### Ejemplo 3: Control de Ventilación en Invernadero
    SI temperatura_interna > 28°C Y humedad_interna > 70% ENTONCES
        encender_ventilador()
    SINO SI temperatura_interna < 18°C ENTONCES
        cerrar_ventanas()  // simulado con un servo o LED
    SINO
        mantener_estado()
    FIN SI

#### Ejemplo 4: Aplicación de Fertilizante según Análisis de Suelo
    LEER ph_suelo, nitrógeno, fósforo

    SI ph_suelo < 5.5 ENTONCES
        aplicar_cal()
    FIN SI

    SI nitrógeno < 20 ppm ENTONCES
        aplicar_fertilizante_nitrogenado()
    FIN SI

    SI fósforo < 10 ppm ENTONCES
        aplicar_fosfato()
    FIN SI

#### Ejemplo 5: Sistema de Riego Nocturno (Evitar Pérdidas por Evaporación)
    LEER hora_actual, humedad_suelo

    SI humedad_suelo < 35% Y (hora_actual >= 18 O hora_actual <= 6) ENTONCES
        activar_riego(10 minutos)
    SINO SI humedad_suelo < 35% Y (hora_actual > 6 Y hora_actual < 18) ENTONCES
        enviar_alerta("Riego no recomendado: alta evaporación")
    FIN SI

### 🔁 ¿Qué son los Ciclos Repetitivos (Bucles)?

Los **ciclos repetitivos** (también llamados **bucles** o **loops**) son estructuras de control que permiten **ejecutar un bloque de instrucciones varias veces**, ya sea un número fijo de veces o mientras se cumpla una condición.

En el contexto agrícola, los ciclos son esenciales cuando necesitas:
- Monitorear múltiples parcelas.
- Tomar lecturas de sensores cada cierto tiempo.
- Aplicar un tratamiento a varias plantas.
- Procesar grandes conjuntos de datos (ej: rendimientos de 100 fincas).

Los dos tipos más comunes son:
- **`PARA` (o `for`)**: cuando sabes **cuántas veces** se repetirá la acción.
- **`MIENTRAS` (o `while`)**: cuando la repetición depende de una **condición que puede cambiar**.

---

### 🌾 Ejemplos de Ciclos Repetitivos en Contextos Agrícolas

#### Ejemplo 1: Riego Automático en 5 Parcelas (Ciclo `PARA`)

    PARA i = 1 HASTA 5 HACER
        LEER humedad_parcela(i)
        SI humedad_parcela(i) < 30% ENTONCES
            activar_riego_parcela(i)
        FIN SI
    FIN PARA
#### Ejemplo 2: Monitoreo Continuo de Temperatura (Ciclo MIENTRAS)
    MIENTRAS sistema_encendido = VERDADERO HACER
        LEER temperatura_actual
        SI temperatura_actual > 35°C ENTONCES
            enviar_alerta("¡Alta temperatura en invernadero!")
        FIN SI
        ESPERAR 10 minutos
    FIN MIENTRAS

#### Ejemplo 3: Aplicación de Tratamiento hasta que Plaga Desaparezca (Ciclo MIENTRAS)
    LEER nivel_plaga

    MIENTRAS nivel_plaga > 5 insectos/planta HACER
        aplicar_tratamiento_biologico()
        ESPERAR 2 días
        LEER nivel_plaga  // nueva medición
    FIN MIENTRAS

    MOSTRAR "Plaga controlada. Tratamiento finalizado."

#### Ejemplo 4: Calibración de Sensor de Humedad (Ciclo PARA)
    PARA intento = 1 HASTA 3 HACER
        LEER valor_sensor
        SI valor_sensor ESTÁ DENTRO DE [28%, 32%] ENTONCES
            MOSTRAR "Sensor calibrado correctamente."
            SALIR DEL CICLO
        SINO
            MOSTRAR "Error en lectura. Reintentando..."
        FIN SI
    FIN PARA

    SI intento > 3 ENTONCES
        MOSTRAR "Falla en calibración. Revisar sensor."
    FIN SI

#### Consejos para Usar Ciclos con Inteligencia
**Evita bucles infinitos:** Siempre asegúrate de que la condición del MIENTRAS pueda volverse falsa.

**Sé claro con los límites:** En un ciclo PARA, define bien el inicio y el fin.

**Combínalos con condicionales:** La verdadera potencia está en usar PARA + SI o MIENTRAS + SI.

**Piensa en eficiencia:** ¿Realmente necesitas revisar 1000 veces? ¿O basta con 10?

        🌱 "Un buen algoritmo no solo repite… repite con propósito." 

### 🌾 Ejemplo Integrado: Sistema de Monitoreo y Riego Automático por Parcelas

#### **Enunciado del Problema**

En una finca experimental con **5 parcelas de cultivo de tomate**, se desea implementar un sistema automatizado que:

1.  **Monitoree diariamente** la humedad del suelo en cada parcela.
2.  **Active el riego solo si** la humedad está por debajo del **35%**.
3.  **Evite regar durante las horas de mayor evaporación** (entre las 10:00 a.m. y las 4:00 p.m.).
4.  El sistema debe **revisar todas las parcelas una vez al día**, preferiblemente al amanecer (6:00 a.m.).

Diseña un algoritmo en pseudocódigo que modele este comportamiento.

---

#### **Algoritmo en Pseudocódigo**


    INICIO
        // Definir constantes
        HUMEDAD_UMBRAL = 35
        HORA_RIEGO_IDEAL = 6  // 6:00 a.m.
        
        // Simular el ciclo diario durante 7 días (una semana)
        PARA dia = 1 HASTA 7 HACER
            MOSTRAR "Día", dia, ": Iniciando monitoreo matutino."
            
            // Revisar cada una de las 5 parcelas
            PARA parcela = 1 HASTA 5 HACER
                LEER humedad_actual DE parcela
                LEER hora_actual  // Suponemos que el sistema sabe la hora
                
                // Decidir si se riega o no
                SI humedad_actual < HUMEDAD_UMBRAL ENTONCES
                    SI hora_actual = HORA_RIEGO_IDEAL ENTONCES
                        activar_riego(parcela, duracion=15 minutos)
                        MOSTRAR "Parcela", parcela, ": Riego activado."
                    SINO
                        MOSTRAR "Parcela", parcela, ": Baja humedad, pero NO es hora óptima. Riego pospuesto."
                    FIN SI
                SINO
                    MOSTRAR "Parcela", parcela, ": Humedad adecuada. No requiere riego."
                FIN SI
            FIN PARA
            
            MOSTRAR "Monitoreo del día", dia, "finalizado."
            ESPERAR 24 horas  // Simular paso al siguiente día
        FIN PARA
        
        MOSTRAR "Semana de monitoreo completada."
    FIN

> 💬 **Cierre de la Sesión 5**  
> Hoy dimos un paso fundamental: pasamos de *pensar* soluciones a *escribirlas con lógica clara*. Aprendiste que los algoritmos no son solo para computadores, sino para **organizar tu propio pensamiento** y convertir decisiones agronómicas en reglas precisas que una máquina puede ejecutar. Al combinar condicionales y ciclos, ya puedes diseñar sistemas que no solo reaccionan al entorno, sino que lo monitorean, analizan y actúan de forma repetitiva y eficiente. 
¡Estás construyendo, paso a paso, la mente de un ingeniero agrónomo del futuro!