<template>
  <v-row justify="center" align="center">
    <v-btn
      color="primary"
      dark
      @click.stop="dialog = true"
      class="animated btn btn-1"
      :class="{'pulse':addClass}"
    >
      Mostrar Caso Real 
    </v-btn>

    <v-dialog
      v-model="dialog"
       hide-overlay
    >
    <v-carousel color='transparent'>
 <githubimgs v-if="videoSrc=='github'"></githubimgs>

 <v-card  v-if="videoSrc=='heroku'" class="text-center" color="orange">
<iframe width="1300px" height="500px" src="https://www.youtube.com/embed/aR3wjq2QDG0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

      </v-card>

  </v-carousel>
    </v-dialog>
  </v-row>
</template>

  

  <script>
  import githubimgs from '@/components/shared/imagesComponent/githubimgs';
  export default {
    props:['video'],
    data () {
      return {
        dialog: false,
        addClass:true,
        videoSrc: this.video ? this.video : 'https://www.youtube.com/embed/RvKoq2ckAFE',
        colors: [
          'primary',
          'secondary',
          'yellow darken-2',
          'red',
          'orange',
        ],
      }
    },
    components:{
      githubimgs
    },
    mounted(){
        setInterval(() => {
          this.addClass = !this.addClass;
        }, 1000);
    }
  }
</script>

<style scoped>
.btn {
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
 /* text-shadow: 0px 0px 10px rgba(0,0,0,0.2);*/
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
 }

/* Demo Stuff End -> */

/* <- Magic Stuff Start */

.btn:hover {
  background-position: right center; /* change the direction of the change here */
  color:black;
  background-image: linear-gradient(to right, #8a2387, #e94057, #f27121);
}

.btn-1 {
  background-image: linear-gradient(to right, #f6d365 0%, #fda085 51%, #f6d365 100%);
}



</style>