### Icons

In this repository we are going to show how we can render icons in svelte pages.

### Svelte Icons

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

#### Icons Library For Svelte Icons

All icons are going to be found on [this](https://svelte-icons-explorer.vercel.app/) page.

### 2. svelte-mono-icons

### Getting started

First you need to install the `svelte-mono-icons` by running the following command:

```shell
yarn add --dev svelte-mono-icons

# or using npm
npm i --save-dev svelte-mono-icons
```

You can search for icons lists in the [mono-icons-repository](https://icons.mono.company/).

### Usage

The mono icons can be used in svelte app as follows:

```svelte
<script>
	 import { MoonIcon, SunIcon, ... } from 'svelte-mono-icons';
</script>

<SunIcon size="1.5x" class="yellow" focusable="false" />
```

### Ref

1. [svelte-icons](https://github.com/Introvertuous/svelte-icons)
2. [svelte-mono-icons](https://www.npmjs.com/package/svelte-mono-icons)
