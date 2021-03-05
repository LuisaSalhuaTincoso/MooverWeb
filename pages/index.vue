<template>
  <div>
    <nav class="navbar navbar-light navColor navbar-expand-sm">
      <div class="container-fluid">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarTogglerDemo01"
          aria-controls="navbarTogglerDemo01"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
          <a class="navbar-brand" href="#"><nuxt-link to="/">Moover</nuxt-link></a>
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link navLink" aria-current="page"
                ><nuxt-link to="/"> Yo Repartidor</nuxt-link></a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link navLink"
                ><nuxt-link to="/"> Yo Empresa</nuxt-link></a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div id="fondo">
      <div class="contents-inicio">
        <h1 class="title-inicio">Moover</h1>
        <p class="us-inicio">
          Quieres un envio rapido y seguro, nos dedicamos a hacerte la vida
          facil
        </p>
        <p class="us-inicio">Donque quieras, cuando quieras</p>
        <br />
        <br />
        <button type="button" class="btn btn-info" @click="goToInicio()">Haz una entrega ya!</button>
        <br />
        <br />
        <button type="button" class="btn btn-success" @click="goToRegistro()">Registrate</button>
      </div>
    </div>
  </div>
</template>
<script>
export default{
  methods:{
    goToInicio(){
      this.$router.push('/inicio_sesion');
    },
    goToRegistro(){
      this.$router.push('/');
    }
  }
}
</script>
<style>
#fondo {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 100%;
  min-width: 320px;
  height: 100vh;
  background-image: linear-gradient(
      rgba(196, 192, 192, 0.5),
      rgba(189, 187, 187, 0.5)
    ),
    url(http://gislinc.com/wp-content/uploads/2015/04/parcel-00.jpg);
  background-position: 50%;
  background-size: cover;
  background-repeat: no-repeat;
}
.title-inicio {
  color: #1f3c88;
  font-weight: 900;
  font-size: 300%;
}
.us-inicio {
  font-weight: bold;
  font-size: 110%;
}

a {
  color: white;
  font-weight: bold;
}
a:hover {
  color: white;
}

.contents-inicio {
  width: 30%;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin: 0% auto;
  margin-top: 9%;
  margin-bottom: 10%;
}

.navColor {
  background: #1f3c88;
}
</style>
