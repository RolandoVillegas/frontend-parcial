<script setup lang="ts">
import { ref } from 'vue'
import ListaPrendas from './ListaPrendas.vue';

// Declaración de tipo para array de prendas.
type IPrenda = {
    id: number,
    nombre: string,
    talle: string,
    color: string,
    precio: number,
    stock: number
}

// Array de prendas (definido por el parcial)
const prendas = ref(
    [
        { id: 1, nombre: 'Camisa Clásica', talle: 'M', color: 'Azul', precio: 50.99, stock: 12 },
        { id: 2, nombre: 'Pantalón Cargo', talle: 'L', color: 'Verde', precio: 89.50, stock: 4 },
        { id: 3, nombre: 'Vestido Veraniego', talle: 'S', color: 'Rojo', precio: 35.00, stock: 0 },
        { id: 4, nombre: 'Chaqueta Denim', talle: 'XL', color: 'Azul', precio: 120.00, stock: 15 },
        { id: 5, nombre: 'Jersey de Lana', talle: 'M', color: 'Gris', precio: 65.75, stock: 6 },
        { id: 6, nombre: 'Short Deportivo', talle: 'S', color: 'Negro', precio: 25.00, stock: 2 },
        { id: 7, nombre: 'Falda Plisada', talle: 'L', color: 'Negro', precio: 45.00, stock: 0 },
    ]
)

// Función para ordenar por precio
function ordenarPorPrecio() {
    prendas.value.sort((a, b) => a.precio - b.precio)
}

// Función para resetear orden.
function resetearOrden() {
    prendas.value.sort((a, b) => a.id - b.id)
}

</script>

<template>
    <main>
        <section>
            <div class="flex flex-col justify-start items-center p-4">

                <div>
                    <button @click="ordenarPorPrecio"
                        class="border rounded bg-blue-900 text-white px-3 py-2 hover:bg-blue-600">Ordenar por
                        precio</button>
                    <button @click="resetearOrden"
                        class="border rounded bg-red-900 text-white px-3 py-2 hover:bg-red-600">Resetear orden</button>
                </div>

                <!-- Llamada a componente para listar prendas -->
                <ListaPrendas :prendas="prendas" />

            </div>
        </section>
    </main>
</template>