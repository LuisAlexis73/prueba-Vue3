<template>
  <button @click="getResult">Click</button>
  <div class="contenedor" v-for="result in results" :key="result.id">
    <p>{{ result.title }}</p>
    <img
      class="img-responsive"
      :src="'https://image.tmdb.org/t/p/w500/' + result.poster_path"
      alt=""
    />
    <div class="overview">
      <p>{{ result.overview }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Base",
  data() {
    return {
      params: {
        api_key: "f4c26714ba3f4672f618f331893d064b",
        with_genres: 27,
      },
      URL: "https://api.themoviedb.org/3/discover/movie",
      results: [],
    };
  },
  methods: {
    setFilter(name, value) {
      this.params[name] = value;
    },
    getResult() {
      axios.get(this.URL, { params: this.params }).then((response) => {
        this.results = response.data.results;
        console.log(this.results);
      });
    },
  },
};
</script>
