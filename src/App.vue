<script>

</script>

<template>

  <article class="container">

    <div class="section topBar noselect">
      <a href="https://github.com/AlexanderNoles" target="_blank"> <img src="./assets/githubLogo.png" alt="" id="logo" class="githubLogo"> </a>
    </div>

    <div class="titleContainer noPointerEvents">
      <h1 class="title font noselect">ALEXANDER NOLES</h1>

      <div class="descriptionTextBlock">
        <h3 class="text font noselect">
          Hi! My name is Alex, I am a recently graduated CS Student who studied at Sussex University. 
          <br>
          <br>
          I am an enthusiastic and artistic, young game developer, looking for an entry level position in the game development industry. 
          I have experience in all parts of game development, from coding to sound design but especially in C# and Unity. 
          In 2022, during my gap year, I released a solo project, called “Dash and Slash”, on the Steam Store. 
          <br>
          <br>
          During my final year of university, I focused my dissertation on emergent narratives and how gameplay influences storytelling. 
          Accordingly, I created a prototype  of a simulation-driven RTS game, that borrowed heavily in style from games such as 
          Kenshi and Stellaris.
          <br>
        </h3>
      </div>
    </div>


    <section class="section noPointerEvents">
      <img class="backingImage noselect" src="./assets/firstBackground.png"/>
    </section>

    <section class="section noPointerEvents displacement1">
      <img class="backingImage noselect" src="./assets/firstBackground.png"/>
    </section>
  
    <section class="section displacement2 noPointerEvents">      
      <div class="dAndSMainAnchor noPointerEvents">
        <div class="dAndSDescription font noPointerEvents">
          <a href="https://store.steampowered.com/app/1951910/Dash_And_Slash/" target="_blank" class="allowPointerEvents noselect">"Dash And Slash"</a> 
          was a project I created during my gap year. It is a full video game (with all the art, code and music produced by me) that I released on the Steam store.
          <br>
          <br>
          Development took several months, during part of which I was also working a regular job. The process taught me a huge amount, particularly in regards to 
          things outside my regular purview of coding. It also solidified my decision to pursue game development as a career despite choosing to do a Computer Science degree.
        </div>
        <img class="dAndSImage noPointerEvents noselect" src="./assets/screenshot7.png"/>
      </div>
      <img class="backingImage noselect" src="./assets/secondBackground-export.png"/>
    </section>
  </article>
  
  
</template>

<style scoped>

  .container{
    position: absolute;
    left: 0%;
    top: 0px;
    height: 100%;
    width: 100%;

    z-index: 100;

    overflow-x: auto;
    overflow-y: scroll;
    scroll-snap-type: y proximity;
  }

  .noPointerEvents{
    pointer-events: none;
  }

  .allowPointerEvents{
    pointer-events: auto;
  }

  .noselect {
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
    -khtml-user-select: none; /* Konqueror HTML */
    -moz-user-select: none; /* Old versions of Firefox */
    -ms-user-select: none; /* Internet Explorer/Edge */
    user-select: none; /* Non-prefixed version, currently
                          supported by Chrome, Edge, Opera and Firefox */
  }

  .titleContainer{
    margin: 10%;
  }

  .font{
    font-family: Arial, Helvetica, sans-serif;
  }

  .title{
    color: white;
  }

  .descriptionTextBlock{
    padding: 10px;
    width: 50%;
    margin-top: 5%;
    margin-left: 50%;
    background-color: black;
  }

  .dAndSMainAnchor{
    top: 5%;
    left: 30%;
    position: absolute;

    height: 100%;
    width: 100%;
  }

  .dAndSImage{
    left: 12%;
    right: 25%;
    position: absolute;

    width: 50%;
  }

  .dAndSDescription{
    z-index: 10000;
    top: 50%;
    left: 12%;
    position: absolute;

    
    width: 50%;
  }

  .text{
    color: white;
  }

  .backingImage{
    width: 100%;
    filter: brightness(70%)
  }

  .section{
    scroll-snap-align: start;
    position: absolute;
    overflow: hidden;
    left: 0%;
    top: 0px;
    z-index: -1000;
    height: 100%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .topBar{
    z-index: 5000;
    width: 100%;
    height: 100px;
    position: absolute ;
  }

  .topBar a{
    float: right;
    text-align: center;
    margin: 10px;
    padding: 2px;
    text-decoration: none;
    font-size: 17px;
    font-family: Arial, Helvetica, sans-serif;
  }

  .githubLogo{
      background: transparent;
      width: 60px;
      height: 60px;
  }

  .displacement1{
    top: 100%;
    z-index: -999;
  }

  .displacement2{
    top: 200%;
    z-index: -998;
  }

</style>
