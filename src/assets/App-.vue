<template> <!-- // ejemplo en 1 solo componente -->
    <h1>Tienda Bit-Game</h1>
  <div class="celeste">
    <p class="uno">¡Bienvenido!</p>
    <hr>
    <p class="dos">A continuacion encontrarás la lista de los juegos que prefieres</p>
  </div>
  <br>
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
        <td><button @click="eliminar(index)"> eliminar</button></td>
      </tr>
      <!-- <tr>
        <td class="gato cero">0</td>
        <td>{{games[0]}}</td>
        <td><button> eliminar</button></td>
      </tr>
      <tr>
        <td class="gato uno">1</td>
        <td>{{games[1]}}</td>
        <td><button> eliminar</button></td>
      </tr>
      <tr>
        <td class="gato dos">2</td>
        <td>{{games[2]}}</td>
        <td><button> eliminar</button></td>
      </tr>
      <tr>
        <td class="gato tres">3</td>
        <td>{{games[3]}}</td>
        <td><button @click="eliminar(index)"> eliminar</button></td>
      </tr> -->
    </tbody>
  </table>

</template>

<script>
//import { indexOf } from 'core-js/js/array';

export default{
    name:'M6-session3',
    props:{
        msg:String,
    },
    data(){
    return{
      games:["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant"]
      };
    },

methods:{
  eliminar(index){
    this.games.splice(index,1)
  }
}
}


</script>

<style>
h1, table{
  background-color: black;
  color: white;
  text-align: center;
}

.celeste{
  background-color: rgb(95, 214, 235);
  align-content: center;
}

.dos{
  font-size: 12px;
}

p{
  padding-left: 20px;
}

button{
  background-color: rgb(190, 15, 15);
  color: white;
  height: 25px;
}

table{
  margin: 0 auto;
  td{
    width: 20cqw;
    height: 30px;
  }
}

.gato{
  width: 20px;
}
</style>
