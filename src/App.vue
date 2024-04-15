<script setup lang="ts">
/* %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */
import { RouterLink, RouterView } from 'vue-router';
import '@mdi/font/css/materialdesignicons.css'
import { fail } from './components/MyConsoleUtil'
/* ----------------------------------------------------------------------------- */

/* %%%%%%  On Page Load %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */


/* %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */
</script>

<template>
	<header>
		<h1 style="text-align: center;">Vue3-Secrets-Analysis-V1</h1>
	</header>

	<RouterView />

	<nav>
		<RouterLink  to="/api" > API </RouterLink>
		<RouterLink  to="/" > Home </RouterLink>
		<RouterLink  to="/dev" > Dev </RouterLink>
	</nav>

</template>

<style scoped>
/* header { line-height: 1.5; max-height: 100vh; } */
/* .logo { display: block; margin: 0 auto 2rem; } */

nav { width: 100%; font-size: 1rem; text-align: center; margin-top: 2rem; }
nav a:hover {background-color: lightcyan}
nav a.router-link-exact-active { color: var(--color-text); }
nav a.router-link-exact-active:hover { background-color: whitesmoke; }
nav a { display: inline-block; padding: 0 1rem; border-left: 1px solid var(--color-border); text-decoration: none; }

/* nav a:first-of-type { border: 0; } */
/* @media (min-width: 1024px) {
  header { display: flex; place-items: center; padding-right: calc(var(--section-gap) / 2); }
  .logo { margin: 0 2rem 0 0; }
  header .wrapper { display: flex; place-items: flex-start; flex-wrap: wrap; }
  nav { text-align: left; margin-left: -1rem; font-size: 1rem; padding: 1rem 0; margin-top: 1rem; }
} */
</style>
