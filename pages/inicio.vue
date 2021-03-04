<template>
<div>    
    <Header/>
    <div class="content justify-content-center">
<div class="row">
        <div class="col-lg-12 col-md-8" >
        <form>
            <div class="form-group">
                <label>Ingresa tu Código de Pedido</label>
                <input type="text" class="form-control" id="codigo Pedido"  aria-describedby="codigoHelp" placeholder="Número de pedido" required>
                <small id="codigoHelp" class="form-text text-muted">Codigo se muestra en la app o en el correo enviado</small>
            </div>
        
            <button type="button" class="btn btn-primary ">Buscar</button>
           
            
        </form>     
    
        </div>
    </div>
    <br>
    <div class="row center">
            <div class="col-lg-12 col-md-8">
                <a  class="btn btn-success">Nuevo pedido!</a>
            </div>
    </div>
        </div>
    
    

    </div>


 
</template>

<script>
  
</script>

<style>

.content{
  width: 25%;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0% auto;
  margin-top: 10%;
  margin-bottom: 10%;
  
}
</style>