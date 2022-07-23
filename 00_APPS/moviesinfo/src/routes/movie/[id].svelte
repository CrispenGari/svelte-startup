<script lang="ts">
  import { page } from "$app/stores";
  import { onMount } from "svelte";
  const id = $page.params.id;
  let movie;
  onMount(async () => {
    const res = await fetch(
      `https://api.themoviedb.org/3/find/${id}?api_key=${
        import.meta.env.VITE_API_KEY
      }&language=en-US`
    );
    const data = await res.json();
    movie = data.results;
    console.log(movie);
  });
</script>

<div class="about">
  <div class="about__movie"><h1>{id}</h1></div>
</div>
