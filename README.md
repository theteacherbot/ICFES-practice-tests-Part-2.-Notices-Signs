# 📚 ICFES Saber 11 English – Part 2
## Notices & Signs

Aplicación web interactiva para practicar la **Parte 2 del examen de Inglés del ICFES Saber 11**, centrada en la interpretación de avisos, letreros y señales breves en contextos cotidianos.

La aplicación está construida en **HTML5, CSS3 y JavaScript Vanilla**, con una interfaz responsive y un sistema de ejercicios generado a partir de un banco de avisos definido localmente en el propio código.

---

## 🎯 Objetivo

Practicar la competencia de interpretación de **Notices & Signs**, mediante preguntas en inglés en las que el estudiante debe identificar **dónde puede encontrar determinado aviso**.

La aplicación presenta:

- Un ejemplo resuelto.
- 5 preguntas por ejercicio.
- Tres opciones de respuesta: **A, B y C**.
- Retroalimentación visual.
- Sistema de puntuación.
- Barra de progreso.
- Cambio entre modo oscuro y claro.
- Generación de nuevos ejercicios a partir de un banco local.

La interfaz identifica explícitamente la actividad como:

> **Part 2 – Notices & Signs**

y presenta la instrucción:

> **Where can you see these notices?**

---

## 🧩 Características principales

### 📝 Ejercicios

Cada ejercicio contiene:

- **1 ejemplo** identificado como pregunta 0.
- **5 preguntas calificables**, numeradas del 1 al 5.
- Un aviso o señal por pregunta.
- Tres opciones de respuesta:
  - A
  - B
  - C
- Una única respuesta correcta.

El ejemplo está bloqueado y muestra previamente la respuesta correcta.

La estructura de la pregunta 0 y de las cinco preguntas calificables está implementada directamente en el motor de ejercicios.

---

## 📢 Avisos y señales

Los avisos se representan visualmente mediante componentes construidos con **HTML y CSS**, en lugar de depender de imágenes externas.

El sistema incluye diferentes estilos visuales para los avisos, entre ellos:

- Paper
- Metal
- Cardboard
- Digital
- Classroom
- Library
- Office
- Glass
- Silver
- Vintage
- Gobelin
- Gold
- Bronze
- Copper
- Wood
- Fabric
- Neon
- Retro
- Minimal
- Elegant
- Rustic
- Modern
- Classic
- Artistic

Estos estilos permiten representar visualmente diferentes tipos de señales y avisos.

---

## 🏫 Contextos

El banco local utiliza diferentes lugares y situaciones como contexto para las preguntas.

Entre ellos:

- School
- Library
- Hospital
- Airport
- Station
- Supermarket
- Park
- Museum
- Hotel
- Restaurant
- Pharmacy
- Shop
- Bus
- Office
- Laboratory
- Zoo
- Elevator
- Waiting room
- Computer room
- Reception

También aparecen otros contextos en los avisos, como:

- Cafe
- Cinema
- Street
- Bakery
- Gallery
- Bank
- Pool
- Beach
- Farm
- Theater
- Market
- Cafeteria
- Club
- Building
- Highway
- Escalator
- Counter
- Home

El banco de avisos está definido directamente dentro de `QuestionGenerator`.

---

## 🔄 Generación de ejercicios

La aplicación incorpora una clase `QuestionGenerator` encargada de construir los ejercicios a partir de plantillas locales.

El banco contiene numerosos avisos predefinidos, por ejemplo:

```text
Lunch for teachers from 12:00 to 1:00 p.m.
Flight BA247 to London - Gate 12
Do not feed the animals
Keep off the grass. Thank you.
Please do not touch the exhibits.
No parking. Violators will be towed.
Fresh bread baked daily.
```

Cada ejercicio selecciona cinco plantillas del banco y genera las alternativas correspondientes.

El sistema utiliza `Math.random()` para variar el orden de las opciones y seleccionar distractores.

---

## 💾 Persistencia local

La aplicación utiliza `localStorage` para conservar el índice del ejercicio.

La clave utilizada es:

```text
icfes_exercise_index
```

El sistema trabaja actualmente con un ciclo de:

```text
15 ejercicios
```

y:

```text
5 preguntas por ejercicio
```

El índice se actualiza después de generar un ejercicio y se almacena localmente en el navegador. 
---

## 📊 Sistema de puntuación

La aplicación dispone de:

- contador de respuestas;
- barra de progreso;
- comprobación de respuestas;
- identificación visual de respuestas correctas;
- identificación visual de respuestas incorrectas.

Durante la práctica se muestra el progreso mediante un formato como:

```text
Puntuación: 0/5
```

La lógica de progreso cuenta únicamente las preguntas 1–5.

---

## ✅ Comprobación de respuestas

El botón:

**Verificar**

comprueba las respuestas seleccionadas.

Las respuestas correctas reciben la clase:

```text
correct
```

Las respuestas incorrectas seleccionadas por el estudiante reciben:

```text
incorrect
```

La aplicación también dispone de un botón:

**Mostrar Respuestas**

que permite visualizar las respuestas correctas.

---

## 🔁 Reiniciar

El botón:

**Reiniciar**

permite borrar las respuestas actuales y comenzar nuevamente el ejercicio.

Se restablecen:

- respuestas del usuario;
- estado de comprobación;
- selección visual;
- respuestas correctas/incorrectas;
- barra de progreso;
- puntuación.



---

## 🌓 Modo oscuro y claro

La aplicación incorpora dos temas visuales:

### Dark

```text
theme-slate-dark
```

### Light

```text
theme-slate-light
```

El usuario puede cambiar entre ambos mediante el botón situado en el encabezado.

Los temas utilizan variables CSS para controlar:

- fondo;
- tarjetas;
- textos;
- bordes;
- colores primarios;
- colores secundarios;
- colores de acento;
- barra de desplazamiento.



---

## 🎨 Diseño visual

La interfaz utiliza un sistema de diseño basado en variables CSS.

Incluye:

- tarjetas;
- bordes redondeados;
- sombras;
- transiciones;
- animaciones;
- botones interactivos;
- barra de progreso;
- componentes visuales para los avisos.

El diseño utiliza una estética moderna tipo plataforma educativa, con una anchura máxima de 1440 px y adaptación a diferentes tamaños de pantalla.

---

## 📱 Diseño responsive

La aplicación incorpora reglas CSS específicas para pantallas pequeñas.

En dispositivos de hasta **768 px**:

- los avisos y opciones pasan a una disposición vertical;
- se reduce el espacio interno;
- los botones ocupan el ancho disponible;
- el encabezado se adapta a pantallas pequeñas.

Está diseñada para funcionar en:

- 💻 Computadores
- 📱 Teléfonos
- 📲 Tablets



---

## 🧱 Arquitectura

El proyecto está implementado en un único archivo HTML que contiene:

```text
HTML
│
├── Estructura de la interfaz
│
├── CSS
│   ├── Temas
│   ├── Componentes
│   ├── Avisos
│   ├── Botones
│   ├── Progreso
│   └── Responsive
│
└── JavaScript
    ├── Estado
    ├── QuestionGenerator
    ├── NoticeStyleManager
    ├── NoticeRenderer
    └── AppController
```

### `NoticeStyleManager`

Gestiona los estilos visuales disponibles para los avisos.

### `QuestionGenerator`

Construye los ejercicios a partir del banco de plantillas locales.

### `NoticeRenderer`

Renderiza:

- ejemplo;
- preguntas;
- avisos;
- opciones;
- estados de respuesta.

### `AppController`

Controla el funcionamiento general de la aplicación:

- inicialización;
- generación de ejercicios;
- cambio de tema;
- reinicio;
- comprobación;
- visualización de respuestas.

La arquitectura y las clases principales están definidas directamente en el JavaScript del documento.

---

## 🌐 Dependencias

El CSS y JavaScript se encuentran incorporados directamente dentro del documento HTML.

Los iconos de la interfaz se implementan mediante **SVG inline**.

Las fuentes utilizan familias disponibles habitualmente en el sistema, como:

```css
Segoe UI
Roboto
Helvetica Neue
Arial
sans-serif
```

Por lo tanto, la interfaz principal no necesita una biblioteca externa de iconos.

---

## ⚙️ Tecnologías

| Tecnología | Uso |
|---|---|
| HTML5 | Estructura |
| CSS3 | Diseño y responsive |
| JavaScript Vanilla | Lógica de la aplicación |
| SVG | Iconos |
| LocalStorage | Persistencia del índice |
| Math.random() | Aleatoriedad local |

---

## 📂 Estructura recomendada del repositorio

```text
icfes-part2-notices/
│
├── part_2.html
└── README.md
```

Si posteriormente se agregan recursos adicionales:

```text
icfes-part2-notices/
│
├── index.html
├── README.md
├── assets/
│   ├── images/
│   └── icons/
└── data/
```

---

## ▶️ Cómo utilizar la aplicación

1. Descargar o clonar el proyecto.
2. Abrir el archivo HTML en un navegador moderno.
3. Esperar la carga del ejercicio.
4. Leer cada aviso.
5. Seleccionar A, B o C.
6. Revisar el progreso.
7. Pulsar **Verificar**.
8. Consultar las respuestas correctas.
9. Pulsar **Nuevo Ejercicio** para continuar practicando.

El controlador de la aplicación inicia automáticamente la generación del primer ejercicio cuando el documento termina de cargarse.

---

## 🎓 Enfoque pedagógico

La actividad está orientada a la práctica de comprensión de avisos y señales breves.

El estudiante debe interpretar el contenido de un aviso y relacionarlo con un lugar o contexto apropiado.

La actividad favorece la práctica de:

- comprensión de mensajes breves;
- identificación de información explícita;
- asociación entre mensaje y contexto;
- reconocimiento de vocabulario cotidiano;
- interpretación funcional del inglés.

---

## 🧪 Ejemplo de funcionamiento

Un aviso como:

```text
Flight BA247 to London - Gate 12
```

se relaciona con:

```text
at an airport
```

Mientras que:

```text
Do not feed the animals
```

se relaciona con:

```text
in a zoo
```

El sistema genera alternativas y registra la respuesta seleccionada por el estudiante.

---

## 📌 Estado actual del proyecto

Esta versión corresponde a una implementación de:

> **Part 2 – Notices & Signs**

Actualmente:

- utiliza un banco local de avisos;
- genera 5 preguntas por ejercicio;
- utiliza 3 opciones de respuesta;
- incluye un ejemplo resuelto;
- permite seleccionar respuestas;
- permite verificar respuestas;
- permite mostrar respuestas;
- incluye puntuación y progreso;
- incluye modo oscuro/claro;
- utiliza `localStorage`;
- genera visualmente los avisos mediante CSS;
- utiliza JavaScript Vanilla.

---

## 🚀 Posibles mejoras

Algunas mejoras que pueden incorporarse en futuras versiones:

- aumentar el banco de ejercicios;
- crear un banco fijo de exámenes completos;
- agregar selección de temática;
- agregar historial de resultados;
- incorporar cronómetro;
- agregar reporte final;
- añadir impresión/guardado en PDF;
- incorporar estadísticas de desempeño;
- agregar niveles de dificultad;
- permitir seleccionar un examen específico;
- separar los datos del banco del motor de renderizado;
- convertir la aplicación en una versión completamente offline con banco de exámenes precargado.

---

## 👨‍🏫 Créditos

**Aplicación:** ICFES Practice Tests – Part 2  
**Sección:** Notices & Signs  
**Autor:** Profesor Édgar Herrera  
**Proyecto:** Exam Engine 2.0

---

## 📄 Licencia

Este proyecto puede adaptarse para fines educativos, institucionales y de práctica académica, respetando las condiciones de distribución y autoría que determine el propietario del proyecto.
