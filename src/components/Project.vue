<template>
  <div v-if="projects">
    <div
      v-for="project in projects"
      :key="project.id"
      class="card pb-3 mb-3"
      style="background-color: #f0f0f0"
    >
      <div class="col-12 col-sm-12 col-md-12 col-lg-10 offset-lg-1 pt-3">
        <h2 class="text-start pb-3 ps-3">{{ project.title }}</h2>
        <div class="row">
          <div class="col-md-7 col-12">
            <div v-if="project.image">
              <CarouselBox :images="project.image" />
              <!-- End carousel -->
            </div>
            <div class="row">
              <div class="col-sm-6 col-md-4 col-4 pb-3">
                <div v-if="project.demo">
                  <a
                    class="btn btn-primary fs-5 text mt-1 ms-2"
                    v-bind:href="project.demo"
                  >
                    <i class="fas fa-laptop-code"></i> Demo
                  </a>
                </div>
              </div>
              <div class="col-sm-6 col-md-4 col-4 pb-3">
                <div v-if="project.github">
                  <a
                    class="btn btn-primary fs-5 text mt-1 ms-0"
                    v-bind:href="project.github"
                    ><i class="fab fa-github"></i> GitHub</a
                  >
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-5">
            <p
              class="fs-15 text text-start ps-3"
              v-for="description in project.description"
              v-bind:key="description"
            >
              {{ description }}
            </p>
            <br />
            <h6 class="ps-3 text-start"><strong>Tecnologías</strong></h6>
            <hr class="ps-1" />
            <div v-for="technology in project.technologies" :key="technology">
              <div class="row">
                <div class="col-md-2">
                  <div v-if="technology.icon">
                    <i
                      class="fa-15x text-start pb-1"
                      v-bind:class="technology.icon"
                    >
                    </i>
                  </div>
                  <div v-else>
                    <img
                      :src="require('@/assets/' + technology.src)"
                      alt="icon"
                      class="pb-1"
                    />
                  </div>
                </div>
                <div class="pl-0 ml-0 col-md-4">
                  <p class="text-center pl-0 align-middle">
                    {{ technology.name }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CarouselBox from "@/components/CarouselBox.vue";

export default {
  components: {
    CarouselBox,
  },
  props: {
    projects: Array,
  },
  mounted() {},
};
</script>

<style>
.fa-15x {
  font-size: 48px;
}
</style>