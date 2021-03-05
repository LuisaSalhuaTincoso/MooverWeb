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
          <a class="navbar-brand" href="#"
            ><nuxt-link to="/">Moover</nuxt-link></a
          >
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
    <div class="container contents-inicio">
      <h3>Inicio de Sesión</h3>
      <br />
      <form >
        <div class="form-group">
          <input
            type="email"
            v-model="email"
            class="form-control"
            placeholder="Ingresa correo"
          />
        </div>
        <div class="form-group">
          <input
            type="password"
            v-model="password"
            class="form-control"
            placeholder="Ingresa contraseña"
          />
        </div>
       
      </form>
      <p v-if="empty" style="color:red;"> Completa los campos</p>
       <button type="submit" class="btn btn-primary" @click="goToInicio()">Ingresar</button>
      <br>
      <br>
      <button class="btn btn-success">Registrarse</button>
    </div>
  </div>
</template>
<script>
export default {
   data: () => ({
     email: null,
    password: null,
    empty: false
   }),
  methods: {
    goToInicio(){
          if(this.email && this.password){
              this.$router.push('/inicio')
          }else{
              this.empty = true
          }
      }
  }
 
};
</script>
