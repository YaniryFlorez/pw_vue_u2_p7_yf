<template>
  <img :src="imagen" alt="No se encontro"/>
  <input v-model="pregunta" type="text" placeholder="Hazme una pregunta" />
    <p>Recuarda que cuando finalices tu pregunta  dar un signo de ?</p>
    <h1>{{pregunta}}</h1>
    <h1>{{respuesta}}</h1>
</template>

<script>
export default {
    data(){
        return{ 
        pregunta: "hola mundo",
        respuesta: null,
        imagen: "https://yesno.wtf/assets/yes/14-b57c6dc03aa15a4b18f53eb50d6197ee.gif",
    };
   },
watch:{
    pregunta(value, olValue){
        console.log(value);
        console.log(olValue);
        if(value.includes('?')){
            console.log("Aqui llamo a la API");
            this.fachada();
        }
},
},

methods:{
    async llamarAPI(){
        const data = await fetch("https://yesno.wtf/api").then((resp) =>
        resp.json()
      );
      console.log(data);
      this.respuesta =data.answer;
      this.imagen = data.image;
      console.log(data);

    },
    async fachada(){
        await this.llamarAPI();

    }
},
};
   
</script>

<style>

</style>