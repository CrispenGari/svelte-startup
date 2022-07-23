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
      `https://api.themoviedb.org/3/movie/popular?api_key=${
        import.meta.env.VITE_API_KEY
      }&language=en-US&page=1`
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
      <input bind:value={searchTerm} type="text" placeholder="Search Movie" />
      <button type="submit"> SEARCH </button>
    </form>
  </div>

  <div class="home__main">
    {#each movies as movie (movie.id)}
      <Movie {movie} />
    {/each}
  </div>
</div>

<style lang="css">
  .home {
    display: flex;
    width: 100%;
    padding: 10px;
    max-width: 1000px;
    margin: 0px auto;
    flex-direction: column;
    height: 90% !important;
  }
  .home__top {
    width: 100%;
  }
  form {
    transition: all 1s;
    border: 1px solid lightgray;
    width: 100%;
    max-width: 400px;
    padding: 3px 5px;
    border-radius: 5px;
    display: flex;
  }
  form > input {
    transition: all 1s;
    flex: 1;
    margin-right: 5px;
    border: none;
    outline: none;
    background-color: #f5f5f5;
    padding: 3px 5px;
    border-radius: 5px;
  }
  form:focus-within {
    border-color: #022540;
    background-color: #022540;
  }
  form > input:focus-within {
    background-color: #022540;
    color: white;
  }
  form > button {
    transform: all 1s;
    display: none;
    background-color: transparent;
    border: none;
    outline: none;
    cursor: pointer;
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
  @media only screen and (max-width: 600px) {
    form {
      margin: 0px auto;
    }
  }
</style>
