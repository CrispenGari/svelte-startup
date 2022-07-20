### Svelte Icons

In this repository we are going to show how we can render icons in svelte pages.

### Installing icons

```shell
npm install --save svelte-icons
```

### Usage Example:

```svelte
<script lang="ts">
	import IoMdTrash from 'svelte-icons/io/IoMdTrash.svelte';
</script>

<div class="app">
	<div class="app__bin">
		<IoMdTrash />
	</div>
</div>

<style>
	.app__bin {
		width: 10px;
	}
</style>
```

### Icons Library

All icons are going to be found on [this](https://svelte-icons-explorer.vercel.app/) page.

### Ref

1. [svelte-icons](https://github.com/Introvertuous/svelte-icons)
