<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <tabla-empresa v-bind:empresas="empresas"/>
  <formulario-empresa @add-Empresa="agregarEmpresa"/>
</template>

<script>
import TablaEmpresa from './components/TablaEmpresa.vue';
import FormularioEmpresa from './components/FormularioEmpresa.vue';
import HelloWorld from './components/HelloWorld.vue'

export default{
  name: 'App',
  components: {
    HelloWorld,
    TablaEmpresa,
    FormularioEmpresa,
  },
  data(){
    return{
      empresas:[
        {
          id_cliente:100,
          nombre_empresa:"VASS",
          ciudad: "Madrid",
          fecha_alta: "06/10/2022"
        },
        {
          id_cliente:200,
          nombre_empresa:"Deloitte",
          ciudad: "Madrid",
          fecha_alta: "06/10/2022"
        },
        {
          id_cliente:300,
          nombre_empresa:"GAZC",
          ciudad: "Madrid",
          fecha_alta: "06/10/2022"
        },
      ]
    }
  },
  methods:{
    agregarEmpresa(empresa){
      this.empresas=[...this.empresas, empresa];
      //this.personas.push(persona); //con typescript
    }      
  }
}

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
