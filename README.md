# Ejemplos básicos del DOM en JavaScript

Este repositorio contiene un **solo ejemplo en HTML** para aprender a manipular el **DOM (Document Object Model)** con JavaScript de forma simple y visual.  
Está pensado para que los principiantes vean cómo interactuar con la página web paso a paso.

---

## 📌 ¿Qué es el DOM?

El **DOM** representa todos los elementos de una página web como objetos que podemos manipular con JavaScript.  
Cada elemento (botón, párrafo, input, div, etc.) se puede **agarrar**, **leer** y **modificar** usando JS.

---

## 🔹 Ejemplo completo en un solo HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Ejemplos DOM Todo en Uno</title>
  <style>
    body { font-family: 'Segoe UI', sans-serif; margin: 20px; background: #f4f4f9; color: #333; }
    h1 { text-align: center; margin-bottom: 30px; color: #222; }
    section { margin: 20px auto; padding: 20px; width: 80%; max-width: 600px; border-radius: 12px; background: white; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
    h2 { margin-bottom: 15px; color: #444; }
    button { padding: 10px 20px; border: none; border-radius: 8px; background: #4f46e5; color: white; font-size: 14px; cursor: pointer; transition: background 0.3s; }
    button:hover { background: #3730a3; }
    #box { width: 100px; height: 100px; background: gray; margin-top: 15px; border-radius: 8px; transition: background 0.3s; }
    input { padding: 10px; width: 100%; font-size: 16px; border: 1px solid #ccc; border-radius: 8px; margin-bottom: 10px; }
    #greeting { font-size: 18px; font-weight: bold; color: #2563eb; }
  </style>
</head>
<body>
  <h1>Ejemplos básicos del DOM</h1>

  <section>
    <h2>1. Detectar un click</h2>
    <button id="btn">Haz click aquí</button>
    <p id="output"></p>
  </section>

  <section>
    <h2>2. Cambiar color con click</h2>
    <button id="colorBtn">Cambiar color</button>
    <div id="box"></div>
  </section>

  <section>
    <h2>3. Formulario en vivo</h2>
    <input id="nameInput" type="text" placeholder="Escribe tu nombre...">
    <p id="greeting">👋 Hola!</p>
  </section>

  <script>
    // Ejemplo 1: Click
    const btn = document.getElementById("btn");
    const output = document.getElementById("output");
    btn.addEventListener("click", () => {
      output.textContent = "¡Me clickeaste! 🎉";
      console.log("Botón clickeado:", btn);
    });

    // Ejemplo 2: Cambiar color
    const colorBtn = document.getElementById("colorBtn");
    const box = document.getElementById("box");
    colorBtn.addEventListener("click", () => {
      box.style.background = box.style.background === "red" ? "gray" : "red";
      console.log("Color cambiado a:", box.style.background);
    });

    // Ejemplo 3: Form en vivo
    const input = document.getElementById("nameInput");
    const greeting = document.getElementById("greeting");
    input.addEventListener("input", () => {
      const name = input.value.trim();
      greeting.textContent = name ? `👋 Hola, ${name}!` : "👋 Hola!";
      console.log("Nombre ingresado:", name);
    });
  </script>
</body>
</html>
