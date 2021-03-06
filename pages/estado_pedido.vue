<template>
    <div>
        <Header/>
        <div class= "estado">
            <h2>Pedido #340</h2>
            <h3 for="">En camino</h3>
            <br>
            <img src="https://ep01.epimg.net/tecnologia/imagenes/2019/11/13/actualidad/1573658897_566202_1573659544_noticia_normal_recorte1.jpg" width="400pt" height="400pt">
            <br>
            <nuxt-link class="link" to="/pedido_detalle">Detalle</nuxt-link>
        </div>
    </div>
</template>
<style>
.estado{
  width: 35%;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0% auto;
  margin-top: 5%;
  margin-bottom: 10%;
  border-radius: 5pt;
  border-style: solid;
  border-color: dimgray;
  padding-bottom: 5%;
  
}
.link{
    color:coral
}
</style>