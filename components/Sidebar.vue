<template>
  <div class="sidebar">
    <div class="liste-des-boutons">
      <button class="Presentation-couleur" @click="scrollingButtons('Debut')">Presentation</button>
      <button class="Presentation-couleur" @click="scrollingButtons('LaPresentation')">Information</button>
      <button class="Presentation-couleur" @click="scrollingButtons('formulaireDeContact')">Contact</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hautDePage: "",
      milieuxDePage: "",
      basDePage: "",
    };
  },

  methods: {
    scrollingButtons(destinationId) {

      // Trouver la div du formulaire de contact par son identifiant (id='...')
      console.log('je viens de cliquer sur le bouton pour aller sur: ', destinationId);
      let element = document.getElementById(destinationId);
      console.log("la je viens de recuperer l'element: ", element);

      // Le rectangle autour de l'element
      let elementRectangle = element.getBoundingClientRect();
      console.log("je viens de recuperer son rectangle: ", elementRectangle);

      let nouvelleCoordonneY = window.scrollY + elementRectangle.y

      console.log('sur le point de scroll vers la coordonnee: ', nouvelleCoordonneY);

      // Cette fonction permet de scroll jusqu'a une certaine coordonnee
      window.scrollTo ({        
        top: nouvelleCoordonneY,
        behavior:'smooth'
      });
      // top: la nouvelle coordonnee pour le haut de l'ecran
      // window.scrollY est la coordonnee Y actuelle
      // elementRectangle.y est la coordonnee Y de l'element cible RELATIVEMENT a l'ecran
    },
  },
};
</script>


<style scoped>
.sidebar {
  background-color: rgb(104, 115, 131);
  height: 100vh;
	width: 100%;
  
}


    

.liste-des-boutons {
  display: flex;
  flex-direction: column;
  text-align: center;
  font-size: 1.125rem;
  line-height: 15rem;
  gap: 10rem;
  width: 100%;
}

/* Les boutons dans la banderole */
button {
  width: 94%;
  border-radius: 20px;
  border: 1px;
  background-color: #0b0b0b;
  position: relative;
  top: 10rem;
  outline: solid rgb(68, 182, 186);
  transition: 1s;
  color: none;
	padding-left: 1rem;
	padding-right: 1rem;
  left: 6px;
}

button:focus {
  transition: 1s;
  color: none;
  outline: 2px solid #851397;
  animation: anim-shadow 0.3s forwards;
  box-shadow: inset rgba(0, 0, 0, 0.35) 2px 2px 12px, #851397 0 0 10px;
}

.Presentation-couleur{
  color: white;

}
</style>
