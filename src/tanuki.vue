<script>

export default{
    name: 'app',
    data() {
      return 
      { 
        count: 0;
        varBool: true
      }
    },
    mounted(){
        if(localStorage.count){
            this.count = parseInt(localStorage.count);
        }
        else{
            this.count = 0;
        }
        this.varBool = true;
        this.$refs.count.innerHTML = this.count;
    },
    methods: {
      randTanuki: function() {
        
        this.varBool = this.varBool? false : this.varBool == false ? null : true;
        this.$refs.tanukiImage.src = "./src/assets/TanukiImages/" + (this.varBool? 'tanuki.jpg' : this.varBool == false ? 'tanuki2.jpg' : 'tanuki3.jpg');

        this.count += 1;
        localStorage.count = this.count;
        this.$refs.count.innerHTML = this.count;
      }
    }
}

</script>

<template>
    <div class="container">
        <div class="tanukiButton">
            <button v-on:click="randTanuki()">
            <h1>Tanuki</h1>
            <div><span ref="count">0</span> tanukis</div>
            </button>
        </div>
            
        <img ref="tanukiImage" class="tanukiImage" src='./assets/TanukiImages/tanuki.jpg'> </img>

    </div>
</template>

<style scoped>

    .container{
        width: 100vw;
        height: 100vh;
        
        top: 0%;
        left: 0%;
        position: absolute;

        background-image: url('./assets/TanukiImages/tanuki.jpg');
        background-size: cover;
        background-attachment: scroll;
    }

    .tanukiButton{
        display: flex;
        flex-direction: column;
    }

    .tanukiImage{
        top: 15%;
        left: 15%;

        width: 70%;

        position: absolute;
    }

</style>