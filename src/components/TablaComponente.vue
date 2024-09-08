
<template>
   
  <br>
  <h1>{{ titulo }}</h1>
  <table>
    <thead>
      <tr>
        <th class="gato">#</th>
        <th>Juego</th>
        <th>Eliminar juego de tu lista</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(game, index) in games" :key="index">
        <td class="gato">{{ index }}</td>
        <td>{{game}}</td>
        <td><button @click="algoMetodo(index)"> eliminar</button></td>
      </tr>
    </tbody>
  </table>

</template>
<script>
    export default {
        name: "TablaComponente",
        props:{
            games:Array,
            titulo: String,
        },
        methods:{
            algoMetodo(index){
                this.$emit("borrar",index)
      }
    }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
