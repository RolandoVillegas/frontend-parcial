# Tailwind CSS - Clases básicas

## 1. Contenedores y tamaño

> w-full → ancho completo
>
> w-1/2, w-1/3 → fracciones del ancho
>
> h-screen → altura igual a la pantalla
>
> min-h-screen → altura mínima de pantalla
>
> max-w-md, max-w-xl → ancho máximo limitado

## 2. Espaciado (padding y margin)

> p-4 → padding en todos lados
>
> px-6 → padding horizontal (x)
>
> py-2 → padding vertical (y)
>
> m-8 → margin en todos lados
>
> mt-4, mb-2 → margin top/bottom

## 3. Flexbox y Grid

> flex → activa flexbox
>
> flex-col, flex-row → dirección columna/fila
>
> items-center → centra verticalmente
>
> justify-center → centra horizontalmente
>
> gap-4 → separación entre hijos
>
> grid → activa grid
>
> grid-cols-2, grid-cols-3 → cantidad de columnas
>
> gap-6 → separación en grid

## 4. Texto

> text-sm, text-base, text-lg, text-xl, text-2xl, text-3xl → tamaños
>
> font-bold, font-semibold, font-light → peso
>
> text-gray-700, text-red-500, text-blue-600 → colores
>
> text-center → texto centrado

## 5. Colores y fondos

> bg-gray-100, bg-blue-500, bg-green-300 → fondo
>
> hover:bg-blue-700 → hover
>
> text-white → texto blanco

## 6. Bordes y redondeado

> border → borde simple
>
> border-2 border-red-500 → borde grueso rojo
>
> rounded, rounded-lg, rounded-full → esquinas redondeadas

## 7. Botones prácticos

> bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-700

# Tailwind CSS - Ejemplos prácticos

## 1. Contenedor centrado en pantalla

\<div class=\"flex items-center justify-center min-h-screen
bg-gray-100\"\>\
\<div class=\"text-center\"\>\
\<h1 class=\"text-3xl font-bold\"\>Hola Mundo\</h1\>\
\<p class=\"text-gray-600\"\>Contenido centrado con Tailwind\</p\>\
\</div\>\
\</div\>

## 2. Lista de tareas

\<ul class=\"bg-white p-4 rounded shadow-md\"\>\
\<li class=\"border-b py-2\"\>Estudiar Vue\</li\>\
\<li class=\"border-b py-2\"\>Comprar pan\</li\>\
\<li class=\"py-2\"\>Llamar a Juan\</li\>\
\</ul\>

## 3. Botón con hover

\<button class=\"bg-blue-500 text-white px-4 py-2 rounded
hover:bg-blue-700\"\>\
Click aquí\
\</button\>

## 4. Tarjeta con imagen y texto

\<div class=\"max-w-sm bg-white rounded-lg shadow-lg
overflow-hidden\"\>\
\<img class=\"w-full h-48 object-cover\"
src=\"https://via.placeholder.com/400x200\" alt=\"Imagen\"\>\
\<div class=\"p-4\"\>\
\<h2 class=\"text-xl font-bold mb-2\"\>Título de la tarjeta\</h2\>\
\<p class=\"text-gray-600 text-sm\"\>Descripción breve del contenido de
la tarjeta.\</p\>\
\</div\>\
\</div\>

## 5. Formulario básico

\<form class=\"bg-white p-6 rounded-lg shadow-lg max-w-md mx-auto
space-y-4\"\>\
\<input type=\"text\" placeholder=\"Nombre\" class=\"w-full border px-3
py-2 rounded\" /\>\
\<input type=\"email\" placeholder=\"Correo\" class=\"w-full border px-3
py-2 rounded\" /\>\
\<button type=\"submit\" class=\"bg-green-500 text-white px-4 py-2
rounded hover:bg-green-700\"\>\
Enviar\
\</button\>\
\</form\>
