# svelte reveal app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit jenaro94/svelte-reveal-template svelte-reveal-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-reveal-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src/slides`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

### Adding new slides

To add a new slide you can add a *.svelte file in the src/slides folder, then import it in index.js following the example.

```
import slide1 from './slide-1.svelte'
import slide2 from './slide-2/index.svelte'
import slide3 from './slide-3.svelte'

export {
    slide1,
    slide2,
    slide3
}
```

### Changing the theme

This template uses [reveal.js](https://revealjs.com/) and [here](https://revealjs.com/themes/) is a list of all the themes, to change the theme simply go to `main.js` and change
`import "../node_modules/reveal.js/dist/theme/black.css";` for another theme, it is important that this import is above other css imports to override the `revealjs.css` file.

### Other customizations

Reveal.js allows for many customizations, transitions, themes, Markdown, Markup, Controls, just visit their [website](https://revealjs.com/) for all of the docs. 


## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).

## Deploying to the web

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
