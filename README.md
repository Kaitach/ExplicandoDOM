# Ejemplos básicos del DOM en JavaScript

Este repositorio contiene ejemplos simples para aprender a manipular el **DOM (Document Object Model)** con JavaScript.  
Está pensado para que los principiantes vean cómo interactuar con la página web paso a paso.

---

## 📌 ¿Qué es el DOM?

El **DOM** es una representación de todos los elementos de una página web.  
Cada elemento (botón, párrafo, input, etc.) se puede **agarrar**, **leer** y **modificar** usando JavaScript.

Ejemplo visual:

```html
<p id="mensaje">Hola</p>
Podemos cambiarlo con JS:

js
Copiar
Editar
document.getElementById("mensaje").textContent = "¡Hola mundo!";
🔹 Ejemplo 1: Detectar un click
html
Copiar
Editar
<button id="btn">Haz click aquí</button>
<p id="output"></p>
js
Copiar
Editar
const btn = document.getElementById("btn");
const output = document.getElementById("output");

btn.addEventListener("click", () => {
  output.textContent = "¡Me clickeaste! 🎉";
  console.log("Botón clickeado:", btn);
});
Qué aprendemos:

getElementById() → agarrar un elemento por su ID.

addEventListener() → escuchar eventos (como click).

textContent → cambiar el texto dentro de un elemento.

🔹 Ejemplo 2: Cambiar estilos
html
Copiar
Editar
<button id="colorBtn">Cambiar color</button>
<div id="box" style="width:100px; height:100px; background:gray;"></div>
js
Copiar
Editar
const colorBtn = document.getElementById("colorBtn");
const box = document.getElementById("box");

colorBtn.addEventListener("click", () => {
  box.style.background = box.style.background === "red" ? "gray" : "red";
  console.log("Color cambiado a:", box.style.background);
});
Qué aprendemos:

.style → acceder a los estilos CSS del elemento.

Podemos cambiar colores, tamaños, bordes, etc.

Se puede alternar valores para crear animaciones simples.

🔹 Ejemplo 3: Input en vivo
html
Copiar
Editar
<input id="nameInput" type="text" placeholder="Escribe tu nombre">
<p id="greeting">Hola!</p>
js
Copiar
Editar
const input = document.getElementById("nameInput");
const greeting = document.getElementById("greeting");

input.addEventListener("input", () => {
  const name = input.value.trim();
  greeting.textContent = name ? `👋 Hola, ${name}!` : "👋 Hola!";
  console.log("Nombre ingresado:", name);
});
Qué aprendemos:

input.value → leer lo que escribe el usuario.

input event → escuchar mientras el usuario escribe, en tiempo real.

Podemos cambiar el contenido de otros elementos dinámicamente.

📝 Resumen de conceptos clave
Concepto	Qué hace	Ejemplo
getElementById	Agarrar un elemento por ID	document.getElementById("btn")
querySelector / querySelectorAll	Seleccionar elementos con CSS selectors	document.querySelectorAll(".cell")
addEventListener	Escuchar eventos (click, input, mouseover...)	btn.addEventListener("click", fn)
textContent	Cambiar el texto dentro de un elemento	p.textContent = "Hola"
style	Cambiar estilos CSS directamente	box.style.background = "red"
input.value	Leer valor de un input	const val = input.value

⚡ Tip para practicar
Agarrá cualquier elemento de la página y cambia su texto o color desde la consola.

Experimentá con addEventListener para que algo suceda cuando hagas click o pases el mouse.

Combina todo: inputs, botones, y divs para crear mini interacciones
