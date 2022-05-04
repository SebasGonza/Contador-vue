<script>
export default {
  data: () => {
    return {
      contador: 2,
    }
  },
  methods: {
    aumentar(){
      this.contador++;
    },
    disminuir(){
      this.contador--;
    },
    resetear(){
      this.contador = 0;
    }
  }
}
</script>

<template>

  <div class="container">
    <img src="./assets/logo.svg" alt="logo vue" width="125" height="125">
   <span> <h1>Hola mundo desde Vue.js 3</h1></span>
    <hr>
    <div class="contador">
      <h2>Contador: {{contador}}</h2>
      <button @click="disminuir();">-1</button>
      <button @click="resetear();">reset</button>
      <button @click="aumentar();">+1</button>

    </div>
  </div>
 
</template>

<style scoped> 
 /* scoped sirve para limitar el alcance que tienen los estilos, en este caso para que los estilos
 se apliquen solo en este archivo */
 .container{
    text-align: center;
 }

.contador{
  font-size: 1.5rem;
}

.contador button{
  border:none;
  border-radius: 5px;
  background-color: #283618;
  color: white;
  text-align: center;
  padding: 13px 20px;
  margin: 12px;
}
.contador button:hover{
  color:black;
  background-color: white;

}

 h1{
   font-weight:bolder;
   color: #6b705c;
 }

 button{
   color: #d4a373;

 }
</style>