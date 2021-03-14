<template>
  <div>
    <div class="landing">
      <div class="container">
        <div class="row">
          <div class="col-sm-12 col-md-5">
            <h3 class="pl-1 title text-white fs-1 text text-start">
              Hey, soy Leo.
            </h3>
            <p class="text-start text-white fs-5 text">
              Un desarrollador apasionado por la programación y por la
              tecnología en general.
            </p>
            <div class="col-md-6 pb-1 text-start">
              <router-link to="/projects" class="btn btn-primary btn-start"
                >Mis proyectos</router-link
              >
            </div>
          </div>
          <div class="col-sm-12 col-md-7 pt-3 mt-3">
            <img class="img-fluid" alt="logo" src="../assets/programming.svg" />
          </div>
        </div>
      </div>
    </div>
    <div>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 200">
        <path
          fill="#212529"
          fill-opacity="1"
          d="M0,64L1440,160L1440,0L0,0Z"
        ></path>
      </svg>
    </div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-sm-12 col-md-12 col-lg-10 offset-lg-1">
          <h3>Habilidades</h3>
          <hr />
          <h5 class="text-start pb-3">Desarrollo Web</h5>

          <h6>Interfaz de usuario</h6>
          <div class="row">
            <Card title="HTML 5" icon="fab fa-html5" />
            <Card title="JS Vanilla" icon="fab fa-js-square" />
            <Card title="CSS 3" icon="fab fa-css3-alt" />
            <Card title="Vue JS" icon="fab fa-vuejs" />
          </div>
          <h6 class="pt-3">Servidor</h6>
          <div class="row">
            <Card title="PHP Con Laravel" icon="fab fa-laravel" />
            <Card title="Node JS" icon="fab fa-node-js" />
          </div>
          <div class="col-md-10 pt-3">
            <hr />
          </div>
          <h5 class="text-start pb-3">Administración de servidores</h5>
          <div class="row">
            <Card title="Linux" icon="fab fa-linux" />
            <Card title="Servidores DNS" src="dns.png" />
            <Card title="HTTPS" src="ssl.png" />
          </div>
          <div class="col-md-10 pt-3">
            <hr />
          </div>
          <h4 class="text-start pb-3">Base de datos</h4>
          <div class="row pb-0 mb-0">
            <Card title="SQL" src="sql.png" />
            <Card title="MySQL" src="mysql.png" />
            <Card title="MongoDB" icon="fas fa-database" />
          </div>
          <div class="col-md-10 pt-3">
            <hr />
          </div>
          <h4 class="text-start pb-3">Aplicaciones de escritorio</h4>
          <div class="row pb-0 mb-0">
            <Card title="Java" icon="fab fa-java" />
            <Card title="C#" src="c-sharp.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from "../components/Header";
import Card from "../components/Card";

export default {
  name: "Home",
  components: {
    Header,
    Card,
  },
};
</script>

<style>
.box {
  /* padding-top: 60px; */
  position: absolute;
  top: 322px;
  width: 100%;
  z-index: 1;
  margin-top: -20px;
  height: 40px;
}

.skills {
  /* padding-top: 60px; */
  position: absolute;
  top: 440px;
  width: 100%;
  z-index: 1;
  /* height: 40px; */
}

.title {
  padding-top: 80px;
  font-size: 32px;
}

.landing {
  /* position: absolute; */
  background-color: #212529;
  margin-top: -10px;
  /* z-index: 1; */
  width: 100%;
  padding-left: 0px !important;
  padding-right: 0px !important;
  height: 4%;
}

.card:hover {
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.08), 0 0;
}
</style>
