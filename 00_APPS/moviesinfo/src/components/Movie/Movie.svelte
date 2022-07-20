<script lang="ts">
  import type { MovieType } from "src/types";
  import { imageURL } from "../../utils";
  export let movie: MovieType;
</script>

<div class="movie">
  <img
    src={`${imageURL}${movie.backdrop_path || movie.poster_path}`}
    alt={movie.id.toString()}
  />
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
    box-shadow: 1px 1px 0px 0px #222;
    width: 300px;
    transition: all 1s;
  }
  img {
    width: 100%;
    border-radius: 5px;
  }
  p {
    font-size: 0.9rem;
    padding: 5px;
    color: gray;
  }
  p > span:first-child {
    font-weight: bold;
  }
  h1 {
    font-size: 1rem;
    padding: 5px;
    text-overflow: ellipsis;
    width: 100%;
    overflow: hidden;
  }
  .movie:hover {
    transform: scale(1.09);
    cursor: pointer;
  }
</style>
