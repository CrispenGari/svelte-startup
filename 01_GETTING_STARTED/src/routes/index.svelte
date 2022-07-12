<script lang="ts">
  console.log("Hello world");

  let counter = 0;
  let text = "";
</script>

<!-- html content goes here -->
<h1>Hello world</h1>
<h1>counter: {counter}</h1>
<h2>{text}</h2>
<input type="text" placeholder="enter anything..." bind:value={text} />
<button
  on:click={() => {
    counter++;
  }}
>
  increment
</button>

<button on:click={() => counter--}>decrement</button>

<style>
</style>
