<template>
  <!-- Partie HTML: Description des elements du site -->
	<!-- <div class="container">
		<div class="navbar-container">
			<nav-bar />
		</div>

		<div class="reste-du-site">
			<re-test />
			<page2 />
		</div>
	</div> -->

  <div class="site-entier">
    <div class="sidebar-parent">
      <sidebar/>
    </div>
    <div class="partie-droite">
      <contenu/>
    </div>
  </div>

</template>

<script>
import Contenu from '~/components/Contenu.vue';
import Sidebar from '~/components/Sidebar.vue';

export default {
	components: {
    Contenu,
    Sidebar,
	}
}
</script>

<style scoped>
.site-entier {
	display: flex;
  flex-direction: row;
  min-height: 100vh;
  height: 100%;
  width: 100vw;
  max-width: 100vw;
  overflow-x: hidden;
}
.sidebar-parent {
	width: 18rem;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
}
.partie-droite {
  min-height: 100vh;
  margin-left: 18rem;
  width: 100%;
}
</style>
