# Svelte

+ [Setup](#setup)
+ [Homepage](#homepage)
  + [Additional Pages](#additional-pages)
+ [Components](#components)

## Setup
Setup a `Svelte` app using the terminal command:

```shell
$ npx sv create
```

Once setup has been completed in the CLI inside the terminal, the packages/dependencies should be installed and the app can be run:

```shell
$ npm run dev -- --open
```

The app can be viewed in the browser here: `http://localhost:5173/`

The initial app structure:

+ `src/routes/+page.svelte` - your home page
+ `src/routes/+layout.svelte` - shared layout (header/footer)
+ `src/lib/` - reusable components
+ `static/` - public assets

## Homepage
When a `Svelte` app is created, the homepage can be found here: `src/routes/+page.svelte`. The code:

```html
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
```

### Additional Pages
To add additional pages, create a folder in the `src/routes/` directory named after the page to be added (e.g. `about`) and add a new `+page.svelte` file to this newly created folder. The new page/route can be viewed here: `http://localhost:5173/about`. This is a `Static Route`, a simple page.

```
src/
  routes/
    +page.svelte          <-- home page (/)
    about/
      +page.svelte        <-- this will become: /about
```

To create a dynamic page, such as a `Blog post`, create a route with parameters in square brackets: `src/routes/blog/[slug]/+page.svelte`. To visit a blog post, the URL would be something like: `http://localhost:5173/blog/hello-world`. 

```
src/
  routes/
    +page.svelte          <-- home page (/)
    about/
      +page.svelte        <-- this will become: /about
    blog/
      [slug]/
        +page.svelte      <-- this is a dynamic page
```

An example page:

```typescript
// src/routes/blog/[slug]/+page.svelte

<script lang="ts">
  import { page } from '$app/stores';
  $: slug = $page.params.slug;
</script>

<h1>Blog Post: {slug}</h1>
```

## Components
A `Component` in `Svelte` is a `.svelte` file containing: markup (`HTML`), styles (`CSS`) and logic (`<script>`). A component can be imported and reused by other components and pages, similar to components in `React`. In `SvelteKit`, components live in `src/lib/` usually in a subfolder like: `src/lib/components/`.

Anything in `src/lib/` can be imported with the `$lib` alias. This alias is built into `SvelteKit` automatically — no config needed. This prevents the need to have ugly relative imports.

```
src/
  lib/
    components/
      Button.svelte
      Card.svelte
      Navbar.svelte
```
