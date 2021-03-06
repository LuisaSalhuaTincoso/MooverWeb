<template>
  <div>
    <Header />
    <br>
    <div class="container">
      <section class="mb-4 contentNew">
        <h2 class="h1-responsive font-weight-bold text-center my-4">
          Tu pedido
        </h2>
        <div class="row">
          <div class="col-md-6 mb-md-0 mb-5">
            <p class="h2-responsive  text-left my-3">Detalles Recojo</p>
            <form name="pedido-form">
              <div class="row">
                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <input
                      type="text"
                      id="name"
                      name="name"
                      class="form-control"
                      :value="post.razonSocial"
                    >
                    <label for="name" class="">Nombre Emisor </label>
                  </div>
                </div>

                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <input
                      type="email"
                      id="email"
                      name="email"
                      class="form-control"
                      :value="post.correo"
                    >
                    <label for="email" class="">Contacto Emisor</label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <div class="md-form mb-0">
                    <input
                      type="text"
                      id="subject"
                      name="subject"
                      class="form-control"
                      :value="post.direccion"
                    >
                    <label for="subject" class="">Dirección Recojo</label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <div class="md-form">
                    <textarea
                      type="text"
                      id="message"
                      name="message"
                      rows="2"
                      class="form-control md-textarea"
                    ></textarea>
                    <label for="message">Referencia</label>
                  </div>
                </div>
              </div>
            </form>
            <p class="h2-responsive  text-left my-3">Detalles Recepcíon</p>
            <form name="pedido-form">
              <div class="row">
                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <input
                      type="text"
                      id="name"
                      name="name"
                      class="form-control"
                    >
                    <label for="name" class="">Nombres Receptor </label>
                  </div>
                </div>

                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <input
                      type="email"
                      id="email"
                      name="email"
                      class="form-control"
                    >
                    <label for="email" class="">Contacto Receptor</label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <div class="md-form mb-0">
                    <input
                      type="text"
                      id="subject"
                      name="subject"
                      class="form-control"
                    >
                    <label for="subject" class="">Dirección Recepcion</label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <div class="md-form">
                    <textarea
                      type="text"
                      id="message"
                      name="message"
                      rows="2"
                      class="form-control md-textarea"
                    ></textarea>
                    <label for="message">Referencia</label>
                  </div>
                </div>
              </div>
            </form>

            <div class="status"></div>
          </div>
          <div class="col-md-6 mb-md-0 mb-5">
            <p class="h2-responsive  text-left my-3">Detalles Paquete</p>
            <form name="pedido-form" @submit.prevent="passes(submit)">
              <div class="row">
                <div class="col-md-12">
                  <div class="md-form mb-0">
                    <input
                      class="form-control-check-input"
                      type="radio"
                      name="flexRadioDefault"
                      id="flexRadioDefault1"
                    >
                    <label
                      class="form-control-check-label"
                      for="flexRadioDefault1"
                    >
                      Paquete grande
                    </label>
                  </div>

                  <div class="md-form mb-0">
                    <input
                      class="form-control-check-input"
                      type="radio"
                      name="flexRadioDefault"
                      id="flexRadioDefault1"
                    >
                    <label
                      class="form-control-check-label"
                      for="flexRadioDefault1"
                    >
                      Paquete mediano
                    </label>
                  </div>
                  <div class="md-form mb-0">
                    <input
                      class="form-control-check-input"
                      type="radio"
                      name="flexRadioDefault"
                      id="flexRadioDefault1"
                    >
                    <label
                      class="form-control-check-label"
                      for="flexRadioDefault1"
                    >
                      Paquete pequeño
                    </label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <select
                      class="browser-default custom-select form-control-select form-select-sm"
                      aria-label=".form-select-sm example"
                    >
                      <option selected
                        >Selecciona categoria de tu pedido</option
                      >
                      <option value="1">Mueble</option>
                      <option value="2">Artefactos</option>
                      <option value="3">Otros</option>
                    </select>
                    <label for="name" class="">Categoria </label>
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <input
                      type="text"
                      id="name"
                      name="name"
                      class="form-control"
                    >
                    <label for="name" class="">Peso aproximado </label>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <div class="md-form mb-0">
                    <select
                      class="browser-default custom-select form-control-select form-select-sm"
                      aria-label=".form-select-sm example"
                    >
                      <option selected>Selecciona vehiculo</option>
                      <option value="1">Moover recomendación</option>
                      <option value="2">Moto</option>
                      <option value="3">Auto</option>
                      <option value="3">Camioneta</option>
                      <option value="3">Camion</option>
                    </select>
                    <label for="name" class="">Vehiculo recomendacion </label>
                  </div>
                </div>
              </div>
            </form>
            <br><br>
            <div class="row content-coti">
              <div class="col-md-12">
                <div class="md-form mb-0">
                  <button class="btn btn-success" @click="cambiar()">
                    Cotizar
                  </button>
                </div>
              </div>
              <div class="cotizacion" v-show="cotizacion">
                <div class="col-md-12">
                  <label>
                    Tiempo pedido:
                  </label>
                  <label>
                    60 minutos
                  </label>
                  <label>
                    -
                  </label>
                  <label>
                    Costo:
                  </label>

                  <label>
                    S/ 12
                  </label>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="text-center text-md-right">
          <button class="btn btn-primary btn-lg">Pedir</button>
        </div>
      </section>
    </div>
  </div>
</template>
<script>
export default {
  async asyncData({  $http }) {
    const post = await $http.$get(`http://mooverapi.azurewebsites.net/api/usuario/1`);
    return { post };
  },

  data() {
    return {
      cotizacion: false,
      
    };
  },
  methods: {
    cambiar() {
      this.cotizacion = !this.cotizacion;
    }

    
  }
  
};
</script>
<style>
.contentNew {
  border-radius: 8pt;
  border-style: solid;
  border-color: powderblue;
  padding: 5%;
}
.content-coti {
  margin: 0 auto;
  margin-left: 5%;
  margin-right: 5%;
}
.cotizacion {
  margin-left: 10pt;
  background: white;
  border-radius: 5pt;
  padding: 20pt;
  margin-top: 14pt;
  font-weight: bold;
}
</style>
