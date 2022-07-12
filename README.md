### Svelte Startup

This repository contains some Svelte applications for cybernatically enhanced web applications.

<img src="/cover.png" width="100%" alt="cover"/>

### Getting Started

First you have to make sure that you have node.js installed on your computer together with the package manager. In my case i will use `yarn` but feel free to use the package manager that you want like `npm`. For the code editor i will be using VSCode so first thing that i will do is to download the `Svelte` extenstion for VSCode and install i. I will download an extenstion called `"Svelte for VS Code"` After installing it go to the settings and edit the `settings.json` and add the following to the `.json` file:

```json
 "[svelte]": {
    "editor.defaultFormatter": "svelte.svelte-vscode"
  }
```

> After you have done that you need to reload the window.

To create a new svelte application you wll run the following command:

```shell
yarn create svelte 01_GETTING_STARTED
# npm
npm create svelte 01_GETTING_STARTED
```

Then you need to answer some couple of questions then next you need to run the following commands:

```shell
cd 01_GETTING_STARTED
# yarn
yarn
yarn run dev

# npm
npm install
npm run dev

```

Then a svelte application will be running on port `3000` and can be accessed at http://localhost:3000/.

We will be working mostly in the `src` folder where there's a `routes` folder by default. Like in next.js a file name is a page router in this folder. So for a home page `/` a file name is `index.svelte`

In a `svelte` file we will have the following structure

```svelte
<script lang="ts">
console.log("Hello world")
</script>

<!-- html content goes here -->
<h1>Hello world</h1>

<style>

</style>

```

### Refs

1. [svelte.dev](https://svelte.dev/)
2. [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_getting_started)
3. [kit.svelte.dev](https://kit.svelte.dev/docs/introduction)
