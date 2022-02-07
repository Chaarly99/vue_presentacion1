<template>
    <h2>Componente Básico</h2>
    <table class="table table-sm">
        <thead>
            <tr>
                <th scope="col">Id Cliente</th>
                <th scope="col">Nombre Empresa</th>
                <th scope="col">Ciudad</th>
                <th scope="col">Fecha Alta</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="empresa in empresas" :key="empresa.id_cliente">
                <th scope="row">{{empresa.id_cliente}}</th>
                <td>{{empresa.nombre_empresa}}</td>
                <td>{{empresa.ciudad}}</td>
                <td>{{empresa.fecha_alta}}</td>
                <td></td>
            </tr>
        </tbody>
    </table>
</template>

<script>

export default {
    name: 'tabla-empresa',
    props:{
        empresas:Array,
    }
}
</script>
<style scoped>
    h2{
        background-color: brown;
    }
    body{
        background-color: coral;
    }
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
    p{
        margin-left: 20px;
        margin-right: 20px;
    }
</style>