<template>
  <div class="landing">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-4 offset-md-1">
          <h3 class="pl-1 title text-white fs-1 text text-start">Contáctame</h3>
          <p class="text-start text-white fs-5 text">
            Si deseas contactarme, puedes completar el siguiente formulario.
          </p>
        </div>
        <div class="col-sm-8 offset-sm-2 col-md-4 pt-3 mt-3 ml-1">
          <img class="img-fluid" alt="logo" src="../assets/contact.svg" />
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
  <!-- Contact form -->
  <div class="container">
    <div class="row">
      <div class="col-md-4 mb-3 offset-md-2 text-start">
        <label for="name" class="form-label text fs-4"> Nombre </label>
        <input type="email" class="form-control" placeholder="" id="inName" />
      </div>
      <div class="col-md-4 mb-3 text-start">
        <label for="email" class="form-label text fs-4">
          Correo electrónico
        </label>
        <input
          type="email"
          class="form-control"
          placeholder="name@example.com"
          id="inEmail"
        />
      </div>
    </div>
    <div class="col-md-8 mb-3 offset-md-2 text-start">
      <label for="description" class="form-label text fs-4">
        Descripción
      </label>
      <textarea class="form-control" rows="4" id="inDescription"></textarea>
    </div>
    <div class="col-md-4 offset-md-4">
      <a class="btn btn-primary text fs-4 p-2 mt-3" @click="sendEmail">
        Contactar
      </a>
    </div>
  </div>
  <!-- end contact form -->
</template>

<script>
import axios from "axios";
import Swal from "sweetalert2";

export default {
  methods: {
    async sendEmail() {
      const name = document.getElementById("inName").value;
      const email = document.getElementById("inEmail").value;
      const description = document.getElementById("inDescription").value;

      const data = {
        name: name,
        email: email,
        description: description,
      };
      //   console.log(data);
      try {
        const res = await axios.post(this.$store.state.url, null, {
          params: {
            name: name,
            email: email,
            description: description,
          },
          mode: "cors",
          headers: {
            // "Access-Control-Allow-Origin": "*",
            Accept: "application/json",
            "Content-Type": "application/json",
          },
        });
        // console.log(res);
        // const response = res.json();
        console.log(res.data);
        if (res.data.message == "success") {
          Swal.fire(
            "¡Perfecto!",
            "He recibido tu correo electrónico. Te contactaré lo antes posible.",
            "success"
          );
        }
      } catch (error) {}
    },
  },
};
</script>