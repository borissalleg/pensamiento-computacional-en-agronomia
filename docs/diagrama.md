# 📊 **Diagramas de Flujo**

> _"Dibuja el camino antes de recorrerlo."_

---

## 🧠 ¿Qué es un **diagrama de flujo**?

Imagina que estás explicando **cómo llegar a la escuela** a un amigo nuevo. No le das un mapa complicado ni le hablas en chino técnico… ¡le dibujas flechas, casitas, semáforos y le dices: “primero giras aquí, luego cruzas allá”!

📌 Eso es un **diagrama de flujo**:  
> Un **dibujo con formas y flechas** que muestra **paso a paso cómo se resuelve un problema o cómo funciona un proceso**.

No usa código, no usa tecnicismos raros… ¡usa dibujitos y lógica! ✏️🧠

---

## 🎯 ¿Para qué sirve?

Sirve para:

- ✅ **Entender procesos complicados** — como cuándo regar un cultivo o cómo calcular la cosecha.
- ✅ **Encontrar errores antes de programar** — si el dibujo no tiene sentido, el programa tampoco lo tendrá.
- ✅ **Trabajar en equipo** — todos entienden el dibujo, aunque no sepan programar.
- ✅ **Aprender a pensar ordenadamente** — ¡como un ingeniero, pero sin tener que serlo todavía!

💡 En el campo, puedes usarlo para:  
- Automatizar riegos 💧  
- Calcular cuánto fertilizante usar 🧪  
- Saber cuándo cosechar según el clima ☀️🌧️

---


### 🧩 Formas que usarías en un diagrama real

En los diagramas de flujo, cada figura tiene un significado especial. Aquí te las dejo con sus usos y una imagen representativa para que las reconozcas fácilmente:

![imagen ](https://tse3.mm.bing.net/th/id/OIP.f0-w0EYsNU0OzojS8ekKXAHaQE?rs=1&pid=ImgDetMain&o=7&rm=3)




## 🛠️ Herramientas online GRATIS para hacer diagramas de flujo

¡No necesitas instalar nada! Con el celular o la laptop puedes hacerlos:

| Herramienta | ¿Qué tiene? | Enlace |
|-------------|-------------|--------|
| **Draw.io (diagrams.net)** | Gratis, sin registro, guarda en Drive o local, formas listas | [https://app.diagrams.net](https://app.diagrams.net) |
| **Lucidchart (Free Tier)** | Muy visual, ideal para presentaciones | [https://www.lucidchart.com](https://www.lucidchart.com) |
| **Canva** | Diseño bonito, plantillas coloridas | [https://www.canva.com](https://www.canva.com) → busca “flowchart” |
| **Whimsical** | Súper intuitivo, ideal para estudiantes | [https://whimsical.com](https://whimsical.com) |

> 💡 **Recomendado para empezar**: `diagrams.net` — es gratis, fácil y no te pide ni correo.

---

## 🌾 Ejemplos concretos en análisis agrícola

### 🌱 Ejemplo 1: ¿Regar o no regar? (Decisión según humedad del suelo)

**Situación:**  
Tienes un sensor que mide la humedad. Si está por debajo de 30%, se riega. Si no, se espera.

#### 🔹 Representación en texto (para entender la lógica)

```plaintext
[INICIO]
    ↓
[LEER humedad del suelo]
    ↓
{¿Humedad < 30%?} —SÍ→ [Activar riego] → [FIN]
               ↓ NO
        [No hacer nada] → [FIN]