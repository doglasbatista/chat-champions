# chat champions front-end

monorepo containing all front-end application fromt the group.

## Technologies used

- [vite](https://vitejs.dev/)
- [vue.js](https://v3.vuejs.org/)
- [turborepo](https://turborepo.org/)
- [yarn](https://classic.yarnpkg.com/lang/en/)

## projects division

the projects are divided into two folder

### apps

- `cerberus`: task manager - [production address](https://cerberus-tau.vercel.app)
- `pythia`: data visualization - [production address](https://pythia-two.vercel.app/)

### packages
- `venus`: design system

## running the application

### install dependencies

in a `node +14` environment, just install the project dependencies:

```bash
yarn
```

## development server

you can start all application server with:

```bash
yarn dev
```

or each invidual one with:

```bash
yarn dev:cerberus
yarn dev:pythia
```

### build

to build all apps and packages, run the following command:

```
yarn run build
```

or each invidual application with:

```bash
yarn build:cerberus
yarn build:pythia
```
