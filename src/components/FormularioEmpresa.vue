<template>
    <h2>Formulario Empresa</h2>
    <form @submit.prevent="enviarFormulario">
        <div class="mb-3">
            <label for="id_empresa" class="form-label">Id Empresa</label>
            <input type="number" v-model="empresa.id_cliente" class="form-control" id="id_cliente" aria-describedby="idClienteHelp">
        </div>
        <div class="mb-3">
            <label for="nombre_empresa" class="form-label">Nombre Empresa</label>
            <input type="text" v-model="empresa.nombre_empresa" class="form-control" id="nombre_empresa" aria-describedby="nombre_empresaHelp">
        </div>
        <div class="mb-3">
            <label for="ciudad" class="form-label">Ciudad</label>
            <input type="text" v-model="empresa.ciudad" class="form-control" id="ciudad" aria-describedby="ciudadHelp">
        </div>
        <div class="mb-3">
            <label for="email" class="form-label">Fecha de Alta</label>
            <input type="date" v-model="empresa.fecha_alta" class="form-control" id="fecha_alta" aria-describedby="fecha_alta_Help">
        </div>
        <button type="submit" class="btn btn-primary">Añadir Empresa</button>
    </form>
    <br>   
</template>
<script>
export default {
    data(){
        return{
            empresa:{
                id_cliente:"",
                nombre_empresa:"",
                ciudad:"",
                fecha_alta:""
            }
        }
    },
    methods:{
        enviarFormulario(){
            this.$emit(`add-Empresa`, this.empresa);
        }
    }
}
</script>
<style scoped>
    h2{
        color: magenta;
    }
    .form-control{
        width: 50%;
        margin-right:auto; 
        margin-left:auto;
    }
    button[type="submit"] {
        background-color: magenta;
        border: none;
    }
</style>