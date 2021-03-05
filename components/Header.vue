<template>
  <div>
    <nav class="navbar navbar-light barColor navbar-expand-sm">
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
            ><nuxt-link to="/inicio">Moover</nuxt-link></a
          >
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link" aria-current="page"
                ><nuxt-link to="/mis_pedidos">Mis Pedidos</nuxt-link></a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link">
                <nuxt-link to="/contacto">Contacto</nuxt-link></a
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<script></script>
<style>
.barColor {
  background: #1f3c88;
}
</style>
