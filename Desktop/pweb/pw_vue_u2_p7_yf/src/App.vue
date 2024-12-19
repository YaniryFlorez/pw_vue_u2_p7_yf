<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Contador/>
  <Contador/>
</template>
 
<script>
import Contador from './components/Contador.vue'
export default {
  name: "App",
  components: {
    Contador
  },
};
</script>
 
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<!--
no es corecto crear las paginas aqui,
aqui se importa las paginas
--los companentes son una estructura o una fraccion de la pagina web
al decir independiente: no quierre decir que no pueda interactuar con otro componente
--los componentes de vue. podemos verlos como piezas de lego.<template>
todos los arcchivos se crean con el .vue y deben estra dentro de la carpeta component
--una pagina es un componente mas. un componente vue y una pagina vue. son lo mismo 
un componente se crea de manera reutilizable.
---
Computed: no recibe elementos
la propiedades computadas guardan el resultado y la ejecucio y si eso no cambia no se vielve a ejecutar
esto pasa por que guarda la informacion en el has
 

  
-->
