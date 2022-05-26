<template>
    <div class="box has-text-weight-bold" :style="estilos">
        <!-- Oque tiver dentro de <Box> sera renderizado de Tarefa.vue -->
        <slot></slot>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    name: 'Box-Modelo',
    data() {
        return {
            estilos: {
                backgroundColor: '#faf0ca'
            }
        }
    }
});
</script>
