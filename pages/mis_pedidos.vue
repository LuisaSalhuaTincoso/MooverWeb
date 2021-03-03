<template>
    <div class="container">
        <nav class="navbar navbar-light bg-light">
            <h1 class="navbar-brand" href="#">
                Mis Pedidos
            </h1>
        </nav>
        <table class="table table-striped">
            <thead>
                 <tr>
                    <th scope="col">#</th>
                    <th scope="col">Pedido</th>
                    <th scope="col">Receptor</th>
                    <th scope="col">Telefono</th>
                    <th scope="col">Fecha Entrega</th>
                    <th scope="col">Estado</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="pedido in pedidos" :key="pedido.id">
                    <td>{{pedido.id}}</td>
                    <td>{{pedido.id}}</td>
                    <td>{{pedido.direccionEntrega}}</td>
                    <td>{{pedido.telefonoEntrega}}</td>
                    <td>{{pedido.fechaentrega}}</td>
                    <td>{{pedido.estado}}</td>
                    
                </tr>
            </tbody>

        </table>

      
    </div>
</template>
<script>
 import axios from 'axios'

  export default {
    data(){
        return {
            pedidos:null
        }
    },
    mounted(){
        this.getPedidos();
    },
    methods:{
        getPedidos(){

                 axios.get("http://localhost:60185/api/pedido")
                 .then( response => {
                     this.pedidos = response.data
                     console.log(response)
                 })
                 .catch( e =>console.log(e))
        }
    }
    
  }

</script>