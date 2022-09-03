<template>
  <div class="q-pa-md">
    <q-carousel animated v-model="slide" arrows infinite :autoplay="autoplay">
      <q-carousel-slide
        :name="1"
        img-src="https://images.unsplash.com/photo-1512950050685-b1d4ae63d2df?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8OHx8d2hpdGUlMjBpbWFnZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
      >
        <h4 class="heading-4">Welcome To! Himanshu's World</h4>
        <p class="Paratag">
          Growing up, I hated school. The sinking feeling I got hearing people .
        </p>
      </q-carousel-slide>

      <q-carousel-slide
        :name="2"
        img-src="https://images.unsplash.com/photo-1619118884592-11b151f1ae11?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTl8fHdoaXRlJTIwaW1hZ2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60"
      >
        <h4 class="heading-4">Log! The Big Picture</h4>
        <p class="Paratag">
          Growing up, I hated school. The sinking feeling I got hearing people .
        </p>
      </q-carousel-slide>
      <q-carousel-slide
        :name="3"
        img-src="https://media.istockphoto.com/photos/modern-white-living-room-with-sofa-coffee-table-cactus-plant-and-picture-id1325341272?b=1&k=20&m=1325341272&s=170667a&w=0&h=mKghxRBYqJYovAirsBI7VhlMHQMb57eN9ANu9zEjtrg="
      >
        <h4 class="heading-4">Make! Your Dream Heiest</h4>
        <p class="Paratag">
          Growing up, I hated school. The sinking feeling I got hearing people .
        </p></q-carousel-slide
      >
      <q-carousel-slide
        :name="4"
        img-src="https://images.unsplash.com/photo-1493723843671-1d655e66ac1c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fHdoaXRlJTIwaW1hZ2V8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60"
      >
        <h4 class="heading-4">Growth! Makes You Better</h4>
        <p class="Paratag">
          Growing up, I hated school. The sinking feeling I got hearing people .
        </p>
      </q-carousel-slide>
    </q-carousel>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref(1),
      autoplay: ref(true),
    };
  },
};
</script>
<style scoped>
.heading-4 {
  text-align: center;
  color: black;
  text-transform: uppercase;
  font-weight: 500;
  letter-spacing: 0.5rem;
  word-spacing: 0.3rem;
  margin-top: 10%;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.Paratag {
  text-align: center;
  color: black;
  text-transform: uppercase;
  font-weight: 500;
  letter-spacing: 0.5rem;
  word-spacing: 0.3rem;
  font-size: 0.9;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
</style>
