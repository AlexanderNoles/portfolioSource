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
      }
    }
}
</script>

<template>

  <article class="container">
    <a href = "./tanuki/" class="secretTanukiButton allowPointerEvents"></a>

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
        </div>
      </div>
    </div>

    <section class="section noPointerEvents">
      <img class="backingImage noselect" src="./assets/firstBackground.png"/>
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

    <section class="section noPointerEvents displacement2">
      gallery
    </section>

    <section ref="DandSSection" class="section displacement3 noPointerEvents">      
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

    <section class="section noPointerEvents displacement4">
      future projects
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

  .descriptionTextBlock{
    color: black;
    margin-top: 10%;
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
    top: 5%;
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

</style>
