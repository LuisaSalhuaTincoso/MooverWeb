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
                            <th scope="col">Receptor</th>
                            <th scope="col">Dir Entrega</th>
                            <th scope="col">Fecha Entrega</th>
                            <th scope="col">Estado</th>
                            <th scope="col">Acción</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="pedido in pedidos" :key="pedido.id">
                            <td>{{pedido.id}}</td>
                            <td>{{pedido.receptor}}</td>
                            <td>{{pedido.direccionEntrega}}</td>
                            <td>{{pedido.fechaentrega}}</td>
                            <td>{{pedido.estado}}</td>
                            <td>
                                <a class ="link" v-show="pedido.estado== 'En camino'"><nuxt-link to="/estado_pedido"><font-awesome-icon :icon="['fas', 'eye']" class="fa-2x"/></nuxt-link></a>
                                <a class ="link" v-show="pedido.estado!= 'En camino'"><nuxt-link to="/pedido_detalle"><font-awesome-icon :icon="['fas', 'eye']" class="fa-2x"/></nuxt-link></a>

                            </td>
                            
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
link{
    color:lightgreen
}
</style>
