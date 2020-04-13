<template>
    <div>
      <div class="jumbotron jumbotron-fluid">
        <div class="container">
          <h3 class="display-3">Treinamento de Vue</h3>
          <p class="lead">Comunicação entre componentes.</p>
        </div>
      </div>
        <div id="app">
            <LVTimes/>
        </div>
    </div>
</template>

<script>
    import LVTimes from "@/components/LVTimes";

    export default {
        name: 'app',
        components: {
            LVTimes
        }
    }
</script>

<style scoped>
    #app {
        margin-left: 10%;
        margin-right: 10%;
        margin-top: 60px;
    }
</style>
