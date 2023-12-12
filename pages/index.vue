<template>
	<div class="container">
		<!--Partie HTML: Description des elements du site-->
		<div class="navbar-container">
			<nav-bar />
		</div>

		<div class="reste-du-site">
			<re-test />
			<page2 />
		</div>
	</div>
</template>

<script>
import ReTest from '@/components/ReTest.vue'
import Page2 from '@/components/Page2.vue'
import NavBar from '@/components/NavBar.vue'

export default {
	components: {
		ReTest,
		NavBar,
		Page2, 
	}
}
</script>

<style scoped>
.container {
	display: grid;
	grid-template-columns: repeat(6, minmax(0, 1fr)); /* Grille de 6 colonnes */
	width: 100vw;
	max-width: 100vw;
	height: 100%;
}
.navbar-container {
	grid-column-start: 1; /* commence a la colonne numero 1 */
	grid-column-end: 2; /* s'arrete a la colonne numero 2 */
	width: 100%;
	height: 100%;
	display: contents;
	position: fixed;
	top: 0;
	left: 0;
}
.reste-du-site {
  color: white;
  align-items: center;
  text-align: center;
	grid-column-start: 2; /* commence a la colonne numero 2 */
	grid-column-end: 7; /* commence a la colonne numero 7 */
	width: 100%;
 }
</style>

<style>
/* Partie CSS non-scoped - sur toute l'application */

/* Parent de tout le monde */
#app {
  /* max-width: 1280px; */
  /* margin: 0 auto; */
  /* padding: 2rem; */
  text-align: center;
  min-width: 100%;
  max-width: 100%;
  display: flex;
  align-items: stretch;
}

/* Background */
body{
  background-color: black;
  background-size: cover;
  min-height: cover;
  min-width: cover;
  max-width: cover;
}

:root {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;

  color-scheme: light dark;
  color: rgba(255, 255, 255, 0.87);
  background-color: #242424;

  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  -webkit-text-size-adjust: 100%;
}

a {
  font-weight: 500;
  color: #646cff;
  text-decoration: inherit;
}
a:hover {
  color: #535bf2;
}

a {
  font-weight: 500;
  color: #646cff;
  text-decoration: inherit;
}
a:hover {
  color: #535bf2;
}

body {
  margin: 0;
  display: flex;
  place-items: center;
  min-width: 320px;
  min-height: 100vh;
}

h1 {
  font-size: 3.2em;
  line-height: 1.1;
}

button {
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.6em 1.2em;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  background-color: #1a1a1a;
  cursor: pointer;
  transition: border-color 0.25s;
}
button:hover {
  border-color: #646cff;
}
button:focus,
button:focus-visible {
  outline: 4px auto -webkit-focus-ring-color;
}

.card {
  padding: 2em;
}

@media (prefers-color-scheme: light) {
  :root {
    color: #213547;
    background-color: #ffffff;
  }
  a:hover {
    color: #747bff;
  }
  button {
    background-color: #f9f9f9;
  }
}
</style>

