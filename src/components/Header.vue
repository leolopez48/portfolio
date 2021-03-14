<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#"><i class="fas fa-code fa-15xs"></i></a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"
          ><i class="fas fa-bars fa-15xs pt-0 mt-0"></i
        ></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <router-link to="/" class="nav-link text-white"> Inicio </router-link>
          <router-link to="/projects" class="nav-link text-white">
            Proyectos
          </router-link>
          <router-link to="/contact" class="nav-link text-white">
            Contáctame
          </router-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style>
.fa-15xs {
  font-size: 32px;
}
</style>