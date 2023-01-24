<template>
  <Base />
</template>

<script>
import Base from "./components/Base.vue";

export default {
  name: "App",
  components: {
    Base,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #1c1c1c;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

p {
  color: whitesmoke;
}

@media (min-width: 425px) {
  .contenedor {
    text-align: center;
  }

  .img-responsive {
    width: 15rem;
  }

  .overview {
    text-align: center;
    width: 80vw;
  }
}
</style>
