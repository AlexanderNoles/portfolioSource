<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

const images = Array.from({ length: 8 }, (_, index) => ({
  id: index + 1,
  url: `/assets/galleryImages/img${index+1}.png`,
}))

const imageDescriptions = new Array(
  "Pixel Art from late 2023.",
  "A planet from Star And Salvation, showcasing both the planet and atmosphere rendering which utilize raymarching. ",
  "Pixel Art based on a postcard from mid 2022.",
  "A hexagonal planet from an extension of my dissertation project. Created as part of an effort to place the simulation directly on a planet.", 
  "Early piece of Pixel Art. Updated fairly recently so it fits a 16:9 aspect ratio.",
  "Pixel Art from late 2022.",
  "An early version of the ship from my dissertation project.",
  "Screenshot of the intro to RED CHAIN, an FPS side-project started inbetween years two and three of university."
)

const config = {
  height: 'auto',
  itemsToShow: 2,
  gap: 5,
  wrapAround: true
}
</script>

<script>
export default {
    name: 'app',
    data() {
      return { n: 0 }
    },
    methods: {
      scrollToGithub: function() {
        const el = this.$refs.githubSection;

        if(el){
          el.scrollIntoView({behaviour: 'smooth'});
        }
      },

      scrollToDissertation: function() {
        const el = this.$refs.dissertationSection;

        if(el){
          el.scrollIntoView({behaviour: 'smooth'});
        }
      },

      scrollToDashAndSlash: function() {
        const el = this.$refs.DandSSection;

        if(el){
          el.scrollIntoView({behaviour: 'smooth'});
        }
      },

      scrollToFuture : function(){
        const el = this.$refs.futureSection;

        if(el){
          el.scrollIntoView({behaviour: 'smooth'});
        }
      }
    }
}
</script>

<template>

  <!-- Fade in effect
  <div class="fadeOutAnimation blackOut noPointerEvents">
  </div>   -->

  <article class="container">
    <a href = "./tanuki/" class="secretTanukiButton allowPointerEvents"></a>

    <div class="contactContainer noPointerEvents font riseUpAnimation">
      <h3>Contact me:</h3>

      <img src="./assets/mailIcon.png" class="mailIcon"></img> alexnoles@outlook.com
    </div>

    <div class="titleContainer noPointerEvents">
      <div class="descriptionTextBlock">
        <div class="descText font noselect">
          <br>
          <br>          
          <br>
          <br>          
          <br>
          <br>
          <h1>About</h1>
          Hi! My name is Alex, I am a recently graduated CS Student who studied at Sussex University. 
          <br>
          <br>
          I am an enthusiastic and artistic, young game developer, looking for an entry level position in the game development industry. 
          I have experience in all parts of game development, from coding to sound design but especially in C# and Unity. 
          In 2022, during my gap year, I released a <a href="#" v-on:click="scrollToDashAndSlash()" class="allowPointerEvents">solo project</a>, called “Dash and Slash”, on the Steam Store. 
          <br>
          <br>
          During my final year of university, I focused my <a href="#" v-on:click="scrollToDissertation()" class="allowPointerEvents">dissertation</a> on emergent narratives and how gameplay influences storytelling. 
          Accordingly, I created a prototype  of a simulation-driven RTS game, that borrowed heavily in style from games such as 
          Kenshi and Stellaris.
          <br>
          <br>
          Many of my projects are stored on my <a href="https://github.com/AlexanderNoles" target="_blank" class="allowPointerEvents">Github</a>, including a lot of my university work.
          I list several of these are in a section <a href="#" v-on:click="scrollToGithub()" class="allowPointerEvents">below</a>.
          <br>
          <br>
          <br>
          Outside of trying to find regular work, I have several <a href="#" v-on:click="scrollToFuture()" class="allowPointerEvents">personal projects</a> that I have been working on intermittently. Each one is similar in scope to Dash And Slash.
          <br>
          <br>
          <br>
          >> <a  class="allowPointerEvents" href="./assets/CV.pdf">My CV</a> <<
        </div>
      </div>
    </div>

    <section class="section noPointerEvents">
      <img class="backingImage noselect slideInAnimation" src="./assets/firstBackground.png"/>
    </section>

    <section ref="dissertationSection" class="section noPointerEvents displacement1">
      <img class="backingImageWrittenSection noselect" src="./assets/dissertationBackground.png"/>

      <div class="dissMainAnchor noPointerEvents">
        <div class="dissDescription font noPointerEvents">
          "Star And Salvation" was the product of my dissertation. The report itself focused on simulated systems and how 
          they could be used to dynamically generate narratives, mainly driven by player decisions. 
          <br>
          <br>
          My simulation took a lot of inspiration from data-centered design and specifically the game engine Bevy's component and entity system, even though my project was created with Unity.
          <br>
          <br>
          During the project (mostly when I didn't want to work on the more complicated stuff), I improved many of my artistic skills. Most of the visual elements in the game utilize 
          raymarching to give them a sense of depth.
          <br>
          <br>
          You can read the report <a class="allowPointerEvents" href="./assets/dissertation.pdf">here</a> and the code repository can be found <a class="allowPointerEvents" href="https://github.com/AlexanderNoles/FinalYearProject">here</a>.
        </div>

        <img class="dissImage noPointerEvents noselect" src="./assets/screenshot8.png"/>
      </div>
    </section>

    <Carousel class="carouselNav carouselDisplacement" v-bind="config">
      <Slide v-for="image in images" :key="image.id">
        <div>
          <img class="carouselItem" :src="image.url"/>
          <p class="carouselDescription font">{{imageDescriptions[image.id-1]}}</p>
        </div>
      </Slide>

      <template #addons>
        <Navigation />
        <Pagination />
      </template>
    </Carousel>

    <section class="section noPointerEvents displacement4">
      <!-- <img class="galleryLogo" src="./assets/GalleryLogo.png"></img> -->

      <img class="backingImage noselect" src="./assets/galleryBackground.png"/>
    </section>

    <section ref="DandSSection" class="section displacement2 noPointerEvents">      
      <div class="dAndSMainAnchor noPointerEvents">
        <div class="dAndSDescription font noPointerEvents">
          <a href="https://store.steampowered.com/app/1951910/Dash_And_Slash/" target="_blank" class="allowPointerEvents noselect">"Dash And Slash"</a> 
          was a project I created during my gap year. It is a full video game (with all the art, code and music produced by me) that I released on the Steam store.
          <br>
          <br>
          Development took several months, during part of which I was also working a regular job. The process taught me a huge amount, particularly in regards to 
          things outside my regular purview of coding. It also solidified my decision to pursue game development as a career despite choosing to do a pure Computer Science degree.
        </div>
        <img class="dAndSImage noPointerEvents noselect" src="./assets/screenshot7.png"/>
      </div>
      <img class="backingImageWrittenSection noselect" src="./assets/secondBackground-export.png"/>
    </section>

    <section ref = "futureSection" class="section noPointerEvents displacement3">
      <img class="backingImage noselect" src="./assets/smallerProjectsBackground.png"/>

      <!-- Two sub descriptions that only appear on hover over -->

      <div class="smallerProjDescription"> 
        <div class="font text">
          Root King, similar to Dash And Slash, started as a Jam game. Unlike Dash And Slash, it was made in two days rather than a week and is my first real puzzle game despite my love for the genre 
          (Dash And Slash was actually meant to have some more exaggerated puzzle elements but the design didn't work). 
          Realistically, this project could be completely finished in a month or two, however, I don't think spending more time on it would be wasteful.
          <br>
          The Jam version can be played <a href="https://emeraldrailgun.itch.io/root-king" target="_blank" class="allowPointerEvents">here</a>.
        </div>
      </div>

      <div class="smallerProjDescription displaceRight"> 
        <div class="font text">
          RED CHAIN was a project I spent the majority of my 2024 summer developing, it is relatively close to being finished but I had to suspend development for the sake of my dissertation. The game focuses on 
          using a chain to hook in enemies so you can use them as weapons. This project is particularly close to being in a releasable state, ideally, I would like to publish it late 2025 or early 2026.
        </div>
      </div>
    </section>

    <section ref="githubSection" class="section noPointerEvents displacement5">
      <img class="backingImage noselect" src="./assets/thirdBackground.png"/>

      <div class="section topBar noselect">
        <a href="https://github.com/AlexanderNoles" target="_blank" class="allowPointerEvents"> <img src="./assets/githubLogo.png" alt="" id="logo" class="githubLogo"> </a>
        <h1 class="title font">Github</h1> <a class="font allowPointerEvents" href="https://github.com/AlexanderNoles" target="_blank">(https://github.com/AlexanderNoles)</a>
      </div>

      <div class="text font githubMainAnchor allowPointerEvents">
        <dl>
        
          <h1>Past Game Jams:</h1>
          <i>(Only includes Submissions with public repositories)</i>
          <br>
          <br>

          <dt>• Root King ( <a href="https://github.com/AlexanderNoles/ld54" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/ld54</a> )</dt>
          <dd> Submission for LD54. Only game jam submission I have made that utlizies Godot instead of Unity. A turn-based puzzle game focused on inputing the correct sequence of inputs. Playable here: <a href="https://emeraldrailgun.itch.io/root-king">Itch.io</a> </dd>
          <br>

          <dt>• Skelli-boi ( <a href="https://github.com/Piturnah/skeliboi" target="_blank" class="allowPointerEvents">https://github.com/Piturnah/skeliboi</a> )</dt>
          <dd> Jam version of a later short-lived released game. I only did art on this project as I was unfamiliar with Unity at the time (early 2020). </dd>
          <br>

          <dt>• Typerope ( <a href="https://github.com/Piturnah/Typerope" target="_blank" class="allowPointerEvents">https://github.com/Piturnah/Typerope</a> )</dt>
          <dd> Group submission for LD49 in 2021. A game similar to twister but utlizing keys on the keyboard instead of coloured circles. Playable here: <a href="https://piturnah.itch.io/typerope">Itch.io</a> </dd>
          <br>

          <dt>• Tri-Colour Gun ( <a href="https://github.com/AlexanderNoles/MiniJam111" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/MiniJam111</a> )</dt>
          <dd> My submission for the 111th mini jam in 2022. Game focused around using several guns with varying weaknesses and strengths. Playable here: <a href="https://emeraldrailgun.itch.io/tri-colour-gun">Itch.io</a> </dd>
          <br>

          <dt>• dread-83 ( <a href="https://github.com/Piturnah/dread-83?tab=readme-ov-file" target="_blank" class="allowPointerEvents">https://github.com/Piturnah/dread-83?tab=readme-ov-file</a> )</dt>
          <dd> Group submission for the 83rd mini jam in 2021. </dd>
          <br>

          <dt>• Minute Long Disaster ( <a href="https://github.com/AlexanderNoles/OneMinuteJam" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/OneMinuteJam</a> )</dt>
          <dd> My submission for the One Minute Jam. Can be downloaded here: <a href="https://emeraldrailgun.itch.io/minutelongdisaster">Itch.io</a> </dd>
          <br>

          <dt>• Dash And Slash (Jam Version) ( <a href="https://github.com/AlexanderNoles/OneButtonJam" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/OneButtonJam</a> )</dt>
          <dd> The original iteration of my gap year project. Build can be downloaded from here: <a href=https://emeraldrailgun.itch.io/bluevsred>Itch.io</a> </dd>
          <br>

          <dt>• Cube-Loop ( <a href="https://github.com/AlexanderNoles/LD47" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/LD47</a> )</dt>
          <dd> My submission for LD47 in 2020. A short game based around using death to progress. Playable here: <a href="./src/cube-loop/index.html">Cube-Loop</a></dd>
          <br>

          <dt>• Sussex Game Jam ( <a href="https://github.com/AlexanderNoles/SussexGameJam" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/SussexGameJam</a> )</dt>
          <dd> Unfinished submission for the Sussex Game Jam. One of the more enjoyable development experiences I've had despite being unable to finish in time.</dd>
          <br>

          <h1>Non-Jam Game Projects:</h1>
          
          <dt>• InfiniPlane ( <a href="https://github.com/AlexanderNoles/InfiniPlane" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/InfiniPlane</a> )</dt>
          <dd> A shell texturing based grass project, based primarily on <a href="https://www.youtube.com/watch?v=9dr-tRQzij4">this</a> video by YouTuber Acerola. </dd>
          <br>

          <h1>University Work:</h1>

          <dt>• World Conqueset ( <a href="https://github.com/AlexanderNoles/SE-Risk" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/SE-Risk</a> )</dt>
          <dd> A recreation of the video game RISK for my Software Engineering module. While this was intended to be a group project it was largely coded by me and one other person. </dd>
          <br>

          <dt>• Shader Basics ( <a href="https://github.com/AlexanderNoles/3DWA" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/3DWA</a> )</dt>
          <dd> Coursework for my 3DWA module. Demonstrates some simplistic fundamental shader techniques but more importantly some model work and use of three.js. 
          Avaliable <a href="https://users.sussex.ac.uk/~an505/">here</a>. </dd>
          <br>

          <dt>• Game Explain ( <a href="https://github.com/AlexanderNoles/LE-Project" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/LE-Project</a> )</dt>
          <dd> A small video games project meant to demonstrate an application of constructivist learning techniques. Coursework for my Technology-Enhanced Learning Environments module. </dd>
          <br>

          <dt>• Computer Networks Coursework ( <a href="https://github.com/AlexanderNoles/CN-Coursework" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/CN-Coursework</a> )</dt>
          <dd> Implementation of TFTP-TCP and TFTP-UDP (both client and server) for my Computer Networks module. </dd>
          <br>

          <dt>• Operating Systems Coursework ( <a href="https://github.com/AlexanderNoles/OS-Coursework" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/OS-Coursework</a> )</dt>
          <dd> Implementation of several task schedulers (and written experiments measuring their performance) for my Operating Systems module. </dd>
          <br>

          <dt>• Past Portfolio ( <a href="https://github.com/AlexanderNoles/ITMPortfolio" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/ITMPortfolio</a> )</dt>
          <dd> A previous iteration of this website, coursework for my ITM module. </dd>
          <br>

          <h1>Other:</h1>
          <dt>• This Website ( <a href="https://github.com/AlexanderNoles/portfolioSource" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/portfolioSource</a> )</dt>
          <dd> My portfolio was made using Vue.js, though I only utilize its structures sparingly. For a smaller website like this I much prefer working mostly without a framework, something Vue allows me to dictate easily.</dd>
          <br>
        
          <dt>• My NEA ( <a href="https://github.com/AlexanderNoles/NEA" target="_blank" class="allowPointerEvents">https://github.com/AlexanderNoles/NEA</a> )</dt>
          <dd> My A-Level NEA. Like many of my projects, this one focused on generation, specifically maze generation. There was some additional code centered around drawing the maze, all done in python.</dd>
          <br>
        </dl>
      </div>
    </section>
  </article>
  
  
</template>

<style scoped>

  a {
    color: rgb(168, 21, 21);
  }

  .blackOut{
    position: fixed;
    top: 0%;
    left: 0%;

    z-index: 1000000000;

    background-color: rgb(0, 0, 0, 0);
    width: 100%;
    height: 100%;
  }

  .smallerProjDescription{
    position: absolute;
    bottom: 1%;
    padding: 1%;
    width: 48%;
  }

  .displaceRight{
    left: 50%;
  }

  .galleryLogo{
    position: absolute;
    padding: 20px;
  }

  .carouselNav{
    --vc-nav-color: white;
    --vc-nav-background: black;
    --vc-nav-border-radius: 5;

    --vc-pgn-active-color: white;
  }

  .carouselDisplacement{
    top: 400%;
    position: absolute;
    width: 100%;
    height: 95%;
  }

  .carouselDescription{
    width: 80%;
    color: rgb(146, 146, 146);
    margin-left: 10%;
  }

  .carouselItem{
    width: 80%;
    margin-left: 10%;
    color: white;
    border-style: solid;
  }

  .secretTanukiButton{
    width: 50px;
    height: 50px;

    position: absolute;
  }

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

    min-width: 1920px;
    min-height: 950px;
    margin: 0 auto;
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
    margin: 2%;
  }

  .font{
    font-family: Arial, Helvetica, sans-serif;
  }

  .title{
    color: white;
  }

  .contactContainer, .contactContainerTop{
    position: absolute;
    right: 1%;
    bottom: 1%;

    color: white;
    background-color: black;
    padding-left: 10px;
    padding-right: 10px;
    padding-bottom: 15px;

    width: 200px;
  }

  .contactContainerTop{
    top: 1%;
    bottom: 93%;
  }

  .mailIcon{
    width: 20px;
    margin-top:
  }

  .descriptionTextBlock{
    color: black;
    margin-top: 10%;
    bottom: 0%;
    padding: 10px;
    width: 25%;
  }

  .githubMainAnchor{
    position: absolute;
    top: 15%;
    left: 5%;
    width: 90%;
    height: 75%;

    overflow-y: scroll;
  }

  .githubMainAnchor dt{
    padding-bottom: 5px;
    padding-top: 5px;
  }

  .githubMainAnchor dd{
    color: rgb(192, 192, 192);
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


  .dissMainAnchor{
    top: 15%;
    right: 20%;
    position: absolute;

    height: 100%;
    width: 100%;
  }

  .dissImage{
    left: 25%;
    width: 50%;
    position: absolute;
  }

  .dissDescription{
    z-index: 10000;
    top: 35%;
    left: 25%;
    position: absolute;
    width: 35%;
    color: white;
  }

  .text{
    color: white;
  }

  .descText{
    color: black
  }

  .backingImage{
    width: 100%;
  }

  .backingImageWrittenSection{
    width: 100%;
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

  .navBar{
    z-index: 10000;
    width: 100%;
    height: 50px;

    bottom: 0%;

    position: fixed;
    background-color: white;
  }

  .topBar{
    z-index: 5000;
    width: 100%;
    height: 100px;
    position: absolute ;
  }

  .topBar a{
    float: left;
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

  .displacement3{
    top: 300%;
    z-index: -997;
  }

  .displacement4{
    top: 400%;
    z-index: -996;
  }

  .displacement5{
    top: 500%;
    z-index: -995;
  }



  .fadeInAnimation{
    animation: fadeIn 1s;
  }

  @keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
  } 

  .fadeOutAnimation{
    animation: fadeOut 1s;
  }

  @keyframes fadeOut {
    0% {  background-color: black; }
    100% { background-color: rgb(0, 0, 0, 0); }
  } 

  .slideInAnimation{
    animation: slideIn 1s;
  }

  @keyframes slideIn {
    0% { padding-left: 100%; }
    100% { padding-left: 0%; }
  } 

  .riseUpAnimation{
    animation: riseUp 0.5s;
  }

  @keyframes riseUp {
    0% { bottom: -100%; }
    100% { margin-top: 1%; }
  } 

</style>
