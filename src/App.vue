<template>
  <h1>Tienda Bit-Game</h1>
  <div class="celeste">
    <p class="uno">¡Bienvenido!</p>
    <hr>
    <p class="dos">A continuacion encontrarás la lista de los juegos que prefieres</p>
  </div>
  <TablaComponente @borrar="eliminarJuego" :games="games" titulo="TITULO TABLA"/>
  <TablaComponente :games="frutas" :titulo="nombre"/>
  <TablaComponente :games="verduras"/>
</template>

<script>
import TablaComponente from './components/TablaComponente.vue';
export default{
    name:'App',
    components:{TablaComponente},
    data(){
    return{
      games:["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant"],
      frutas: ['banana', 'manzana'],
      verduras: ['papa', 'zanahoria', 'zapallo', 'acelga'],
      nombre: 'La tabla de las frutas, esto es para mi, no forma parte de la prueba'
      };
    },
    methods: {
      eliminarJuego(index) {
        console.log('Eliminando...', this.games[index]);
        this.games.splice(index, 1);
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
