<template>
  <div>
    <h1>Directivas</h1>
    <hr/>
    
    <h1>v-text</h1>
    <span v-text="titulo" ></span>
    <h1>{{titulo}}</h1>
    <hr/>


    <h1>v-show</h1>
    <h3>tu edad es : {{edad}}</h3>
    <h2 v-show="edad>=18" >Mayor de edad</h2>
    <h2 v-show="edad<18" >Menor de edad</h2>
    <hr/>

    
    <h1>v-if v-else-if vi-else</h1>
    <h3>tu edad es : {{edad}}</h3>
    <h2 v-if="edad>=18 && edad >0 && edad<100" >mayor de edad</h2>
    <h2 v-else-if="edad<18 && edad >0 && edad<100" >menor de edad</h2>
    <h2 v-else >Edad invalida</h2>



    <button @click="inc()">incrementar</button>
    <button @click="dis()">disminuir</button>

    <h1>v-html</h1>
    <div v-html="html" ></div>
    <hr/>
   


  </div>
</template>

<script>
  export default{
    data: () => ({
      titulo: 'Hola desede vue3',
      html: "<h3>Soy un H3</h3>",
      edad:0,

    }),
    methods:{
      inc(){
        this.edad++;
      },
      dis(){
        this.edad--;
      }
    },
  };
</script>
<style scoped>
  div{
    text-align: center;
    margin: 0px 2rem;
  }
  h2{
    color: brown;
  }
</style>
