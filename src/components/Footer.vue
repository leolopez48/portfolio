<template>
  <div class="box-footer">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 300">
      <path
        fill="#212529"
        fill-opacity="1"
        d="M0,256L1440,288L1440,300L0,300Z"
      ></path>
    </svg>
  </div>
  <footer class="footer bg-dark">
    <p class="text-white pt-3">
      Copyright © 2021 Leonel López. <br />
      Todos los derechos reservados.
    </p>
    <img :src="require('@/assets/made.png')" alt="" />
  </footer>
</template>

<style>
/* .box-footer {
  height: 100px;
} */
.footer {
  /* position: absolute; */
  /* top: 700px; */
  height: 120px;
  /* z-index: 1; */
}
</style>