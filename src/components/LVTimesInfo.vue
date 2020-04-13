<template>
    <div>
        <h2>Time Selecionado</h2>
        <div v-if="lista!==undefined">

            <p>Time:{{ lista.nome | formata }}</p>
            <p>Rival: {{ lista.rival | formata }}</p>
            <p>Estadio: {{ lista.estadio | formata }}</p>
        </div>


    </div>


</template>

<script>
    export default {
        props: {
            lista: Object,

        },
        filters: {
            formata(selecionado) {
                selecionado = selecionado.toUpperCase()
                return selecionado
            }
        }

    }
</script>

<style scoped>

</style>
