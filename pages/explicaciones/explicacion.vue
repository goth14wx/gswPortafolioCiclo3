<template>

<v-layout row >
    <v-flex lg12>
        <animeTitle1 style="padding-left:15px" :title="'Problemas en la Nube'" />
    </v-flex>
    <v-flex lg12>
        <cardParagraph :textCard="textCard" :linksCard="links" :classAdd="'card01'" :fancy="true" />
         <v-row align="center" justify="center" data-aos="fade-up-left">
 <iframe src="https://giphy.com/embed/HExOLXcToOVPO" width="480" height="307" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
  </v-row>
    </v-flex>
     <v-flex lg12>
         <cardParagraph :textCard="textCardStep1" :classAdd="'card02'" :fancy="true">
             <animeTitle2 :tClass="'step1'" :txtString="'NO TARJETA DE CREDITO, NO AVANCE'" />
         </cardParagraph>
         <v-row align="center" justify="center" data-aos="fade-down-right">
<iframe src="https://giphy.com/embed/l3vRaak6fltTSi6xW" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
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
            stepsVideo:['https://www.youtube.com/embed/AIslRC6L494'],
            textCard:'Me vi en problemas a la hora de realizar ciertas guias para las cuales necesitaba de una tarjeta de credito/debito para poder realizar las guias',
            links:[
                {
                     to:'https://cloud.google.com/free/docs/gcp-free-tier?hl=es',
                    text:'GCP USO GRATUITO',
                    color:"red"
                }
            ],
            textCardStep1:"GCP no permite poder hacer uso de sus tecnologias si es que no mira un posible comprador en puerta, pero hay muchas soluciones en la nube mejor pensadas para una startup o un pequeño desarrollador que solo desea saber como funciona PaaS u otros servicios que ofrecen otras empresas",

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

