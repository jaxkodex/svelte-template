# sv

Everything you need to build a Svelte project, powered by [`sv`](https://github.com/sveltejs/cli).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```sh
# create a new project
npx sv create my-app
```

To recreate this project with the same configuration:

```sh
# recreate this project
npx sv@0.15.4 create --template minimal --types ts --add prettier eslint tailwindcss="plugins:typography" --install yarn svelte-template/
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```sh
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```sh
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.

## UI components

UI components come from [shadcn-svelte](https://shadcn-svelte.com) using Phosphor icons. Imports use the `#lib` alias, which maps to `src/lib`:

```sh
# add a component, e.g. button or select
yarn shadcn-svelte add button

# sync yarn.lock after the CLI installs dependencies
yarn install
```

Generated components live in `src/lib/components/ui` and are excluded from ESLint and Prettier, since they are meant to be regenerated rather than hand-maintained. Shared helpers live in `src/lib/utils.ts`.
