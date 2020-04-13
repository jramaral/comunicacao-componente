<template>

        <li class="list-group-item">
            <span>{{lista.nome}} </span>
            <button @click="Selecionar" class="btn btn-success float-right">Selecionar</button>

        </li>

</template>

<script>
export default {
    props:{
        lista:{
            type: Object
        }
    },
    methods:{
        Selecionar(){
            this.lista.nome.toLowerCase()

            this.$emit("selecionarTime",this.lista)
        }
    }
}
</script>
