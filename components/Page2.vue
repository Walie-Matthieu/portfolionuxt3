<template>
  <div class="body">
    <h1 id="LaPresentation" class="le-titre">Hi, I am Walie M. Hoummad</h1>

    <h2 class="le-texte">
      I'm a french newbie on the front-developement, I currently study HTML CSS
      and JavaScript
      <br />
      I usually work with Visual studio code, all parts of my website have been
      created with this tool
      <br />
      Here is my portfolio!

    </h2>

    <div class="flex-parcour">
      <div class="miit">
        <div>MIIT</div>
        <div>CCNA</div>
        <div>ITIL Foundation</div>
      </div>

      <div class="cyber">
        <div>Cyber Sécurité</div>
        <div>ISO 27001</div>
        <div>RGPD</div>
      </div>

      <div class="front-end">
        <div>HMTL,CSS</div>
        <div>Javascript</div>
      </div>
    </div>

    <p class="flex-icon">
      <a
        class="linkedin"
        href="https://www.linkedin.com/in/walie-hoummad-089727238/"
        target="_blank"
      >
        <img src="@/res/linkedin.png" height="50" title="Linkedin" 
        width="70"
      />
      </a>

      <a
        class="Git-Hub"
        href="https://github.com/Walie-Matthieu"
        target="_blank"
        
      >
        <img src="@/res/git-hub-logo.png" height="70" title="git-hub" 
        width="120"
        style="position: absolute; top: -13%;"/>
      </a>

    </p>

    <div class="lettre" id="formulaireDeContact">
      <div class="container">
        <h3>Contact me here</h3>

        <form class="formulaire">
          <div class="wrapper">
            <div class="box">
              <label for="fname">First Name</label>
              <input type="text" name="fname" />

            </div>

            <div class="box">
              <div class="mail">
                <label for="lname">Mail</label>
                <input type="text" name="lname" />
              </div>
            </div>
          </div>

          <div class="wrapper">
            <div class="box">
              <label for="tel">un message</label>
              <textarea type="text" name="tel" required></textarea>
            </div>
          </div>
          <div class="le-preums">
            <input
              class="submit-button"
              type="submit"
              name=""
              value="send message"
            />
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      laPoutre: false, // est-ce qu'on affiche la poutre
    };
  },
  methods: {
    // Quand on clique sur la zone de texte
    activerLaPoutre() {
      if (this.laPoutre === false) {
        this.laPoutre = true;
      } else if (this.laPoutre === true) {
        this.laPoutre = false;
      }
    },
  },
};
</script>

<style scoped>
/* le flex de tout les icons */
.flex-icon {
  position: relative;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 5rem;
  top: 50px;
  left: 0%;
}

.linkedin {
  color: rgb(12, 131, 241);
}

/* Ne pas oublier de changer Git-Hub de position */
.Git-Hub {
  color: rgb(0, 0, 8);
}

.body {
  background-color: rgb(3, 3, 73);
  background-size: cover;
  min-height: 100vh;
  min-width: 100%;
  max-width: cover;
  
}

.flex-parcour {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  justify-content: space-evenly;
}

.miit {
  padding: 20px;
  font-size: 30px;
  flex-direction: row;
  border: 1px solid #0b8cb8;
  box-shadow: inset rgba(0, 0, 0, 0.35) 2px 2px 12px, #0b8cb8 0 0 10px;
}

.cyber {
  padding: 20px;
  font-size: 30px;
  flex-direction: row;
  border: 1px solid #dc6211;
  box-shadow: inset rgba(0, 0, 0, 0.35) 2px 2px 12px, #c0460d 0 0 10px;
}

.front-end {
  padding: 20px;
  font-size: 30px;
  flex-direction: row;
  border: 1px solid #0bb833;
  box-shadow: inset rgba(0, 0, 0, 0.35) 2px 2px 12px, #0bb82e 0 0 10px;
}

.lettre {
  margin: 0;
  padding: 0%;
  /* top: 0px; */
  /* position: relative; */
  box-sizing: border-box;

  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  width: 80%;
  padding: 20px;
  background: rgb(4, 41, 4);
  transition: all 0.2s;
  border: 0px solid red;
  border-radius: 15px;
}

.container:hover {
  border: 4px solid red;
  transition: all 0.2s;
  box-shadow: inset rgba(0, 0, 0, 0.35) 2px 2px 12px, #c0460d 0 0 10px;
}

.container h3 {
  color: white;
  font-size: 3em;
  text-align: center;
  margin-bottom: 20px;
}

.formulaire {
  display: flex;
  flex-direction: column;
  gap: 20px;
  align-items: flex-end;
}

.wrapper {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 30px;
}

.wrapper .box {
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 2px;
}

.wrapper .box input {
  width: 100%;
  font-size: 20px;
  border: none;
  outline: solid;
  outline-color: cyan;
  outline-width: 0px;
  height: 2rem;
  background-color: rgb(71, 63, 63);
}

label {
  position: relative;
}

.wrapper .box input:focus {
  outline-width: 2px;
  /* transition: 0.5s ease; */
}

.wrapper .box .la-barre {
  background-color: blueviolet;
  width: 100%;
  height: 2px;
}

.le-preums {
  position: relative;
  background-color: rgb(28, 98, 116);
  z-index: 0;
  /* height: 30px; */
  border-radius: 12px;
}

.submit-button {
  background-color: blue;
  border-color: aqua;
  height: 150%;
  position: relative;
  z-index: 10;
  top: -8px;
  cursor: pointer;
  transition: 0, 25s;
  border-radius: 12px;
  color: white;
}

.submit-button:active {
  top: -1px;
}

textarea {
  background-color: rgb(71, 63, 63);
  width: 100%;
  height: 10rem;
  border-width: 0px;
  border-bottom-width: 4px;
  border-style: solid;
  border-image: linear-gradient(
      90deg,
      rgba(109, 0, 204, 1) 0%,
      rgba(0, 0, 0, 0) 0%
    )
    1;
  transition: all 0.6s;
}

textarea:focus {
  outline: none !important;
  border-image: linear-gradient(
      90deg,
      rgba(109, 0, 204, 1) 99%,
      rgba(0, 0, 0, 0) 100%
    )
    1;

  transition: all 0.6s;
}

.mail {
  width: 100%;
  height: 1rem;
  border-width: 0px;
  border-bottom-width: 1px;

  border-image: linear-gradient(
      90deg,
      rgba(109, 0, 204, 1) 0%,
      rgba(0, 0, 0, 0) 1%
    )
    1;
  transition: all 0.6s;
}

.mail:focus {
  border-image: linear-gradient(
      90deg,
      rgba(109, 0, 204, 1) 99%,
      rgba(0, 0, 0, 0) 100%
    )
    1;
  transition: all 0.6s;
}

.le-texte{
  text-decoration: none;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.le-titre{
  text-decoration: none;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
