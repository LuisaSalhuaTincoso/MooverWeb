<template>
    <div>
        <Header/>
        <br>
        <div class="container">
            <div class="titlezone">
                <form>
                    <div class="row">
                        <div class="col-lg-8">
                            <label class = "lWhite"></label>
                        </div>
                        <div class="col-lg-4">
                        <input type="text" class="form-control" placeholder="Código de pedido">
                        
                        </div>
                    </div>
                </form>
            </div>
               
                <br>
                <table class="table table-striped table-responsive-sm">
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
<style >
.titlezone{
    background: #0070b8;
    padding: 10pt;
}
.lWhite{
    color:white;
    font-size: medium;
}
</style>
