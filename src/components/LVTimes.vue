<template>
    <div class="row">
        <div class="col-8">
            <ul class="list-group list-group-flush">
                <LVTimesLista v-for="t in lista" :key="t.id" :lista="t" @selecionarTime="timeSelecionado=$event" :class="itemAtivo(t)"/>
            </ul>
        </div>
        <div class="col-4">
            <div>
                <LVTimesInfo :lista="timeSelecionado"/>
            </div>
        </div>


    </div>

</template>

<script>
    import LVTimesLista from "@/components/LVTimesLista";
    import LVTimesInfo from "@/components/LVTimesInfo";

    export default {
        components: {
            LVTimesLista,
            LVTimesInfo
        },
        data() {
            return {
                lista: [
                    {id: 1, nome: "santos", estadio: 'vila belmiro', rival: 'são paulo'},
                    {id: 2, nome: "grêmio", estadio: 'arena grêmio', rival: 'internacional'},
                    {id: 3, nome: "palmeiras", estadio: 'alianzz parque', rival: 'corinthias'},
                    {id: 4, nome: "cruzeiro", estadio: 'mineirão', rival: 'atletico mineiro'},
                    {id: 5, nome: "bahia", estadio: 'arena fonte nova', rival: 'vitória'},
                    {id: 6, nome: "flamengo", estadio: 'maracanã', rival: 'vasco'},
                ],
                timeSelecionado: undefined

            }
        },
        methods:{
            itemAtivo(item){
                return{
                    active: this.timeSelecionado && this.timeSelecionado.id === item.id
                }
            }
        }

    }

</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
