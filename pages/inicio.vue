<template>
  <div>
    <Header />
    <div class="contents justify-content-center">
      <div class="row">
        <div class="col-lg-12 col-md-8">
          <form>
            <div class="form-group">
              <font-awesome-icon :icon="['fas', 'cube']" class="fa-4x" />
              <label>Ingresa tu Código de Pedido</label>
              <input
                type="text"
                class="form-control"
                id="codigo Pedido"
                aria-describedby="codigoHelp"
                placeholder="Número de pedido"
                
              >
              <small id="codigoHelp" class="form-text text-muted"
                >Codigo se muestra en la app o en el correo enviado</small
              >
            </div>

            <button
              type="button"
              class="btn btn-primary "
              @click="goToPedido()"
            >
              Buscar
            </button>
          </form>
        </div>
      </div>
      <br>
      <div class="row center">
        <div class="col-lg-12 col-md-8">
          <button type="button" class="btn btn-success" @click="goToNuevo()">
            Nuevo pedido!
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    goToPedido() {
      this.$router.push("/estado_pedido");
    },
    goToNuevo() {
      this.$router.push("/pedido");
    }
  }
};
</script>

<style>
.contents {
  width: 25%;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0% auto;
  margin-top: 5%;
  margin-bottom: 5%;
  border-radius: 8pt;
  border-style: solid;
  border-color: powderblue;
  padding: 5%;
}
</style>
