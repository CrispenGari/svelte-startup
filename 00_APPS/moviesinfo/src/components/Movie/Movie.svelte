<script lang="ts">
  import type { MovieType } from "src/types";
  import { imageURL } from "../../utils";
  export let movie: MovieType;
</script>

<div class="movie">
  <a href={`/movie/${movie.id}`}>
    <img
      loading="lazy"
      src={`${imageURL}${movie.backdrop_path || movie.poster_path}`}
      alt={movie.id.toString()}
    /></a
  >
  <h1>{movie.title}</h1>
  <p>
    <span> Released Date:</span>
    <span>
      {movie.release_date}
    </span>
  </p>
</div>

<style>
  .movie {
    display: flex;
    flex-direction: column;
    cursor: pointer;
    margin: 5px;
    border-radius: 5px;
    width: 300px;
    transition: all 1s;
    border: 1px solid lightgray;
  }
  img {
    width: 100%;
    border-radius: 5px;
  }
  p {
    font-size: 0.8rem;
    padding: 5px;
    color: gray;
  }
  h1 {
    font-size: 1rem;
    padding: 5px;
    text-overflow: ellipsis;
    width: 100%;
    overflow: hidden;
    font-weight: 500;
    text-transform: uppercase;
  }
  .movie:hover {
    transform: scale(1.09);
    cursor: pointer;
  }
</style>
