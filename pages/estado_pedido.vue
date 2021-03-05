<template>
    <div>
        <Header/>
        <div class= "estado">
            <h2>Pedido #340</h2>
            <h3 for="">En camino</h3>
            <iframe src="https://goo.gl/maps/hJ2HGG9M8Wbv37QM6" frameborder="0"></iframe>
            <a><nuxt-link to="/pedido_detalle">Mas detalle</nuxt-link></a>
        </div>
    </div>
</template>
<style>
.estado{
  width: 25%;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0% auto;
  margin-top: 5%;
  margin-bottom: 10%;
  border-radius: 5pt;
  border-style: solid;
  border-color: dimgray;
  
}
</style>