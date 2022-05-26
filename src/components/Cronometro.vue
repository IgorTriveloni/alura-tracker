<template>
    <section>
        <strong class="display">{{ tempoDecorrido }}</strong>
    </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
    name: "Cronometro-Modelo",
    props: {
        tempoEmSegundos: {
            type: Number,
            default: 0
        }
    },  
    computed: {
        //00:00:00 cronometro
        tempoDecorrido(): string {
            return new Date(this.tempoEmSegundos * 1000).toISOString().substr(11, 8);
        },
    },
});
</script>

<style scope>
.display {
    color: var(--texto-primario);
}
</style>