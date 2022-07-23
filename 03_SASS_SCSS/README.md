### Svelte, Sass and Scss

In this readme we are going to guide on how to create style components using `sass` and `scss` in svelte.

### Installation

First you need to install the following packages

```shell
# using npm
npm install sass --save-dev

# using yarn
yarn add -D  sass
```

In your `svelte.config.js` you go ahead and add the following to it:

```js
import adapter from '@sveltejs/adapter-auto';
import preprocess from 'svelte-preprocess';
/** @type {import('@sveltejs/kit').Config} */
const config = {
	preprocess: preprocess(),

	kit: {
		adapter: adapter()
	}
};

export default config;
```

Now in your `svelte` component you can be able to use `scss` for styling here is an example:

```svelte
<script lang="ts">
</script>

<div class="app">
	<div class="app__bin">
		<h1>Hello world</h1>
	</div>
</div>

<style lang="scss">
	.app {
		.app__bin {
			h1 {
				color: red;
			}
		}
	}
</style>
```

You can also be able to use `sass` by just changing the `lang` attribute from `scss` to `sass`. Here is an example:

```svelte
<style lang="sass">
	.app 
		.app__bin
			h1
				color: red
</style>
```

### Ref

1. [stackoverflow.com](https://stackoverflow.com/questions/61140275/how-to-use-scss-in-use-svelte-3)
