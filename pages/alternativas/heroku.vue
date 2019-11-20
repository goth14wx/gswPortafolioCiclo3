<template>

<v-layout row>
    <v-flex lg12>
        <animeTitle1 style="padding-left:15px" :title="'HEROKU, escula para mi'" />
    </v-flex>
    <v-flex lg12>
        <cardParagraph :textCard="textCard" :linksCard="links" :classAdd="'card01'" :fancy="true" />
    </v-flex>
     <v-flex lg12>
         <cardParagraph :textCard="textCardStep1" :classAdd="'card02'" :linksCard="linksPort" :fancy="true">
             <animeTitle2 :tClass="'step1'" :txtString="'Paso #1- crear la app'" />
         </cardParagraph>
       <window :sliceTxt="'composer create-project ASP'" :txt="'composer create-project laravel/laravel --prefer-dist nombreDeLaAppDeLaravel'" :customClass="'terminal1'" />
    </v-flex>

 
<!----->
    <v-flex lg12>
         <cardParagraph :textCard="textCardStep2" :classAdd="'card00'"  :fancy="false" >
             <animeTitle2 :tClass="'step2'" :txtString="'Paso #2- GIT la clave'"/>
         </cardParagraph>
       <window :sliceTxt="'git add'" :rootUser="true" :txt="'git commit -am \'message\''" :customClass="'terminal2'" />
    </v-flex>

   <v-flex lg12>
         <cardParagraph :textCard="textCardStep3" :classAdd="'card02'"  :fancy="true">
             <animeTitle2 :tClass="'step3'" :txtString="'paso #3 archivo para heroku \'\'procfile\'\''" />
         </cardParagraph>
       <window :sliceTxt="'apt-ge'" :txt="'echo \'web: vendor/bin/heroku-php-apache2 public/\' > Procfile'" :customClass="'terminal3'" />
<cardParagraph :textCard="textCardStep4" :classAdd="'card03'"  :fancy="true"/>
        <window :sliceTxt="'git add'" :rootUser="true" :txt="'git commit -am \'message\''" :customClass="'terminal4'" />
<cardParagraph :textCard="textCardStep5" :classAdd="'card04'"  :fancy="true"/>
          <window :sliceTxt="'heroku login'" :txt="'heroku create'" :customClass="'terminal5'" />
         
    </v-flex>

  <v-flex lg12>
         <cardParagraph :textCard="textCardStep6" :classAdd="'card05'"  :fancy="false" >
             <animeTitle2 :tClass="'step4'" :txtString="'Paso #3- Preparando la heroku-cli!'"/>
         </cardParagraph>
       <window :sliceTxt="'heroku log'" :rootUser="false" :txt="'heroku config:set APP_KEY=$(php artisan --no-ansi key:generate --show)'" :customClass="'terminal6'" />
         
    </v-flex>

     <v-flex lg12>
         <cardParagraph :textCard="textCardStep7" :classAdd="'card06'"  :fancy="false" >
             <animeTitle2 :tClass="'step5'" :txtString="'Paso #3- Git push y listo!'"/>
         </cardParagraph>
 <window :rootUser="false" :sliceTxt="'git push -u mast'" :txt="'git push heroku master'" :customClass="'terminal9'" />
         <cardParagraph :textCard="textCardStep8" :classAdd="'card06'"  :fancy="false"/>
         <h2 class="text-center font-darker-grotesque"> PUEDES VER EL SITIO DESDE ESTE ENLACE!!
             <br>
             <a href="https://obscure-beyond-92031.herokuapp.com/" target="_blank">https://obscure-beyond-92031.herokuapp.com/</a>
         </h2>
    <br/>
        <customModalDialog :video="'heroku'"/>
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
            textCard:'HEROKU es de esas empresas que saben que es dar un servicio sencillo pero pontente, pensando siempre en esa facilidad, es muy pero que muy conveniente para sacar un proyecto rapido y facil, ademas de que sus planes no son exagerados es mas son mas accesibles que cualquier otra plataforma, me refiero a la calidad / precio, ni que hablar de lo "ergonomico" que es trabajar en esta plataforma',
            links:[
                {
                    to:'https://www.heroku.com/pricing',
                    text:'HEROKU PRICES',
                    color:'pink'
                }
            ],
            linksPort:[
                {
                    to:'https://getcomposer.org/',
                    text:'COMPOSER'
                },
                 {
                    to:'https://laravel.com/',
                    text:'laravel',
                    color:'red'
                }
            ],
            textCardStep1:"Laravel es un framework que tambien fue lo primero, lo mas cercano que llegue a tener con un framework MVC, ahora lo ocupo mas reactivo, pero es muy buena opcion si tu primer lenguaje de programacion que aprendiste para desarrollo web",
            textCardStep2:"agregamos y hacemos un commit a nuestro repositorio local claro, primero tienes que hacer un git init",
            textCardStep3:"Muy bien ahora solo falta poder agregar el archivo procfile que solo carga un perfil para nuestro deploy en heroku, claro todo esto dentro de la app que creamos",
             textCardStep4:"Volvemos a agregar y hacer un commit",
            textCardStep5: "ahora si, creamos nuestra app de heroku, antes debes de loguearte en tu cuenta desde la heroku-cli solo corriendo \'heroku login\' y listo",
            textCardStep6:"Necesitamos de un pequeño retoque nada mas ",
            textCardStep7:"Ahora solamente hacemos push al repositorio remoto que ya heroku ha preparado para recibir la app",
            textCardStep8:"Ahora ya esta tu app en heroku, puedes abrirla desde la consola con \'heroku open\'"
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

