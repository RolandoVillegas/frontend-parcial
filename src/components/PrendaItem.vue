<script setup lang="ts">

type IPrenda = {
    id: number,
    nombre: string,
    talle: string,
    color: string,
    precio: number,
    stock: number
}

const props = defineProps({
    prenda: {
        type: Object as () => IPrenda,
        required: true
    }
})  
</script>

<template>
    <div class="border-2 border-gray-300 rounded-lg p-3">
        <div class="text-xl font-semibold ">{{ props.prenda.nombre }}</div>
        <div class="text-sm text-gray-500">Talle: {{ props.prenda.talle }}</div>
        <div class="text-sm text-gray-500">Color: {{ props.prenda.color }}</div>
        <div class="text-l  text-black">Precio: ${{ props.prenda.precio }}</div>
        <div class="text-sm text-gray-500">
            <span v-if="props.prenda.stock === 0" class="text-red-500">
                Stock: {{ props.prenda.stock }}
            </span>
            <span v-else-if="props.prenda.stock <= 5" class="text-yellow-500">
                Stock: {{ props.prenda.stock }}
            </span>
            <span v-else class="text-green-500">
                Stock: {{ props.prenda.stock }}
            </span>
        </div>
    </div>
</template>