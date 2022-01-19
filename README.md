## chat champions front-end

monorepo containing all front-end application fromt the group.

## Technologies used

- [vite](https://vitejs.dev/)
- [vue.js](https://v3.vuejs.org/)
- [turborepo](https://turborepo.org/)
- [yarn](https://classic.yarnpkg.com/lang/en/)

# Turborepo starter

This is an official Yarn v1 starter turborepo.

## projects division

the projects are divided into two folder

### applications

- `cerberus`: task manager
- `pythia`: data visualization

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
