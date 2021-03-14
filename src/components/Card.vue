<template>
  <div class="col-6 col-sm-6 col-md-3 col-lg-3">
    <div class="card mt-1">
      <div class="card-title pt-3">
        <div v-if="icon">
          <i class="fab fa-3x" v-bind:class="icon"></i>
        </div>
        <div v-else>
          <img :src="require('@/assets/' + src)" alt="Icono" />
        </div>
      </div>
      <div class="card-body">{{ title }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    icon: String,
    src: String,
  },
};
</script>