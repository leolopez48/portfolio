<template>
  <div class="landing">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-4 offset-md-1">
          <h3 class="pl-1 title text-white fs-1 text text-start">
            Mis Proyectos
          </h3>
          <p class="text-start text-white fs-5 text">
            Estos son algunos de los proyectos en los que he trabajado.
          </p>
        </div>
        <div class="col-sm-8 offset-sm-2 col-md-4 pt-3 mt-3 ml-1">
          <img class="img-fluid" alt="logo" src="../assets/projects.svg" />
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
  <div class="container">
    <div class="row">
      <Project :projects="projects" />
    </div>
    <div class="row text-start pt-3 mt-3">
      <div class="col-md-12">
        <h6 class="text fs-2">¿Deseas ver más proyectos?</h6>
        <p class="text fs-5">
          Puedes entrar en mi GitHub para ver los códigos fuentes de todos mis
          proyectos.
        </p>
        <a
          href="https://github.com/leolopez48"
          class="btn btn-primary text fs-4"
          ><i class="fab fa-github text fs-2 pt-1"> </i> GitHub</a
        >
      </div>
    </div>
  </div>
</template>

<script>
import Project from "@/components/Project.vue";
import projects from "../assets/projects.json";

export default {
  components: {
    Project,
  },
  data() {
    return {
      projects: [],
    };
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      const data = projects.projects;
      this.projects = JSON.parse(JSON.stringify(data));
    },
  },
};
</script>

<style>
.landing {
  background-color: #212529;
  margin-top: -10px;
  width: 100%;
  padding-left: 0px !important;
  padding-right: 0px !important;
  height: 4%;
}

.fs-15 {
  font-size: 1rem;
}
</style>