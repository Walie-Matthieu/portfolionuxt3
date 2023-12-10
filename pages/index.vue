<template>
	<div>
		<!--Partie HTML: Description des elements du site-->
		<nav-bar class="navbar" />

		<div class="pour-les-jolies-couleurs">
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
.pour-les-jolies-couleurs {
  color: white;
  flex-grow: 10;
  align-items: center;
  text-align: center;
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

