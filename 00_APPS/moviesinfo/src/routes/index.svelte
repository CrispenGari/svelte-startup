<script lang="ts">
  import Movie from "../components/Movie/Movie.svelte";
  import type { MovieType } from "src/types";

  import { onMount } from "svelte";
  let searchTerm: string = "";

  let movies: Array<MovieType> = [];
  let loading = true;

  onMount(async () => {
    loading = true;
    const res = await fetch(
      "https://api.themoviedb.org/3/movie/popular?api_key=5ac0ad7d8ec61646a043f5cda245e111&language=en-US&page=1"
    );
    const data = await res.json();
    loading = false;
    movies = data.results;
    console.log(movies);
  });
</script>

<div class="home">
  <div class="home__top">
    <form action="">
      <label for="search-input" />
      <input bind:value={searchTerm} type="text" />
      <button type="submit"> SEARCH </button>
    </form>
  </div>

  <div class="home__main">
    {#each movies as movie (movie.id)}
      <Movie {movie} />
    {/each}
  </div>
</div>

<style>
  .home {
    display: flex;
    width: 100%;
    padding: 10px;
    max-width: 1000px;
    margin: 0px auto;
    flex-direction: column;
    height: 90% !important;
  }
  .home__main {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    overflow-y: scroll;
    overflow-x: hidden;
    padding-bottom: 10px;
    padding-top: 10px;
  }
  .home__top {
    padding: 10px;
    border-bottom: 1px solid lightgray;
  }
  .home__main::-webkit-scrollbar {
    display: none;
  }
</style>
