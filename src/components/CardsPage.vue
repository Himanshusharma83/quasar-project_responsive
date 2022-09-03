<template>
  <div class="div">
    <img
      class="img"
      src="https://images.unsplash.com/photo-1582233479366-6d38bc390a08?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZmFjZXN8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60"
    />
    <q-separator class="sep" vertical inset color="black" />
    <div>
      <h5 class="heading">
        Some Word's
        <hr width="150" class="line" />
      </h5>

      <p class="paratag">
        Due to this, you need to use paragraph transitions in all your essays.
        You have to make sure that you are choosing the right words to start a
        paragraph. In this section, we are going to look as some examples of
        sentence starters.
      </p>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {};
  },
};
</script>
<style scoped>
.div {
  display: flex;
  gap: 10rem;
}
.img {
  margin-left: 5%;
  border-radius: 5%;
}
.heading {
  color: black;
  margin-left: 5rem;
  font-weight: 500;
  text-transform: uppercase;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.line {
  margin-right: 58%;
}
.paratag {
  margin-left: -25%;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  letter-spacing: 0.1rem;
  word-spacing: 0.1rem;
}
@media (min-width: 300px) and (max-width: 700px) {
  .img {
    text-align: center;
    width: 90%;
  }
  .sep {
    display: none;
  }
  .paratag {
    letter-spacing: 0;
    word-spacing: 0;
    margin-left: 5%;
  }
  .div {
    display: inline-block;
  }
}
</style>
