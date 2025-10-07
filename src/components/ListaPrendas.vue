<script setup lang="ts">
import PrendaItem from './PrendaItem.vue';

type IPrenda = {
    id: number,
    nombre: string,
    talle: string,
    color: string,
    precio: number,
    stock: number
}

const props = defineProps({
    prendas: {
        type: Array as () => IPrenda[],
        required: true
    }
})

</script>

<template>
    <div class="flex flex-col justify-start sm:flex-row  mt-4 gap-3">
        <div v-for="prenda in props.prendas"
            class="flex flex-row justify-between items-center ">
            <PrendaItem :prenda="prenda" />
        </div>
    </div>
</template>