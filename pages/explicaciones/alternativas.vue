<template>

<v-layout row>
    <v-flex lg12>
        <animeTitle1 style="padding-left:15px" :title="'ALTERNATIVAS PARA PEQUEÑOS DESARROLLADORES'" />
    </v-flex>
    <v-flex lg12>
         
        <cardParagraph :textCard="textCard" :linksCard="links" :classAdd="'card01'" :fancy="true" >
            <animeTitle2 :tClass="'step1'" :txtString="'Heroku'"/>
        </cardParagraph>
        <v-row align="center" justify="center" data-aos="fade-down-right">
 <v-img
      src="http://davidtaylor.codes/img/techlogos/heroku.png"
      lazy-src="https://picsum.photos/id/11/10/6"
      aspect-ratio="1"
      class="grey lighten-2"
      max-width="500"
    ></v-img>
             </v-row>
    </v-flex>
     <v-flex lg12>
         <cardParagraph :textCard="textCardStep1" :linksCard="linksNetlify" :classAdd="'card02'" :fancy="true">
          <animeTitle2 :tClass="'step2'" :txtString="'Netlify'"/>  
         </cardParagraph>
             <v-row align="center" justify="center" data-aos="fade-down-right">
 <v-img
      src="https://www.netlify.com/img/press/logos/logomark.png"
      lazy-src="https://picsum.photos/id/11/10/6"
      aspect-ratio="1"
      class="grey lighten-2"
      max-width="500"
    ></v-img>
             </v-row>
    </v-flex>
<!----->
    <v-flex lg12>
         <cardParagraph :textCard="textCardStep2" :classAdd="'card03'" :linksCard="linksGithub" :fancy="false" >
             <animeTitle2 :tClass="'step3'" :txtString="'GITHUB PAGES'"/>
         </cardParagraph>
        <v-row align="center" justify="center" data-aos="fade-down-right">
<iframe src="https://giphy.com/embed/du3J3cXyzhj75IOgvA" width="480" height="469" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
  </v-row>
    </v-flex>





</v-layout>

</template>


<script>
import animeTitle1 from '@/components/shared/customTitles/animeTitle1';
import animeTitle2 from '@/components/shared/customTitles/animeTitle2';
import cardParagraph from '@/components/shared/cardParagraph';
import window from '@/components/shared/window';
import alert from '@/components/shared/alert';
import customModalDialog from '@/components/shared/customModalDialog';
export default {
    data(){
        return{
            stepsVideo:['https://www.youtube.com/embed/SsEBgZoMBng'],
            textCard:'HEROKU ha sido, una solución, mas que una solución es una maravilla de soluciones en la nube, con ella empece a desplegar mis primeras aplicaciones, ademas de no necesitar de una tarjeta de credito, aun para sus poderosos plugins, aunque tiene una limitante ya que solamente puedes tener base de datos de POSTGRESQL pero con su util plugin de cleardb, puedes escribir asi tambien tu base de datos en mysql',
            links:[
                {
                    to:'https://www.heroku.com/about',
                    text:'ACERCA DE HEROKU',
                    color:'purple'
                }
            ],
            linksNetlify:[
                {
                    to:'https://www.netlify.com/about/',
                    text:'ACERCA DE NETLIFY',
                     color:'green'
                },
                
            ],
            linksGithub:[
                {
                    to:"https://pages.github.com/",
                    text:'ACERCA DE GITHUB PAGES',
                    color:"black"
                }
            ],
            textCardStep1:"Netlify me empezo a dar una solucion aun mas dosil, pequeña, pero versatil, no esta tan pensada para grandes equipos pero muy bien para pequeñas aplicaciones, que no necesiten de mucha carga, esta muy bien diseñada para frameworks front-end como lo son VUE.JS, ANGULAR REACT.JS",
            textCardStep2:"en este caso github pages ofrece una buena solucion para poder mostrar tu trabajo, solo puede desplegar una aplicacion sin backend, esta muy bien para poder hacer un serverless sin mas",
            
        }
    },
    components:{
animeTitle1,
animeTitle2,
cardParagraph,
window,
customModalDialog,
alert
    }

}
</script>

