# Vue3-Secrets-Analysis-V1

This project is based on a 'clean' Vue3 boiler-plate with important additions and configurations. It is well suited for 'bootstrapping' a new vue3 application.

```sp
The project uses the Vue3 Composition API.
```

This project contains these packages:
<table>
	<tr>
		<td width="10%">
		<td>Vite
		<td>Vuetify
		<td>Pinia
		<td>Vue Router
		<td>Prettier
	</tr>
	<tr>
	<td width="10%">
		<td>TypeScript
		<td>Lint
		<td>Babel
		<td>MDI Fonts
		<td width="10%">
	</tr>
</table

***
***

# Details

This project began with a BIOLER PLATE Vue 3 build generated like this;

```sh
$ npm create vue@latest
```
The following options were selected:

✔ Add TypeScript?	== 		**Yes**<br>
✔ Add JSX Support?	==		**Yes**<br>
✔ Add Vue Router for Single Page Application development?	==		**Yes**<br>
✔ Add Pinia for state management?	==		**Yes**<br>
✔ Add Vitest for Unit Testing?	==		**No** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <== Look <br>
✔ Add an End-to-End Testing Solution?	==		**No**&nbsp;&nbsp;&nbsp; <== Look <br>
✔ Add ESLint for code quality?	==		**Yes**<br>
✔ Add Prettier for code formatting? 	==		**Yes**<br>

After the initial build completed, these packages were also installed:

✔ Vuetify\
✔ Babel\
✔ MDI Fonts

***
Most of the boiler-plate code generated by [ npm createVue@latest ] has been discarded.
This includes all of the existing components and views. The existing CSS is disabled.

The myConsoleUtil.ts component is added to improve debugging.
Multiple changes to the TypeScript/Lintr configuration are added to prevent the most annoying features. 
App.vue contains template and script modifications that verify/confirm the installed packages.

<table><tr><td width="5%"></><td >
Note:<br>
The package versions will, over time, become out of date. $ npm update will update all packages. The developer is cautioned that new versions could introduce breaking changes.

</td></tr></table>

***


# ORIGINAL README.md Comments

These comments were retained, with a few edits, for general reference.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
    1) Run `Extensions: Show Built-in Extensions` from VSCode's command palette
    2) Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```