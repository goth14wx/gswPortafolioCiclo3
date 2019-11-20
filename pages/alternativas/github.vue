<template>

<v-layout row>
    <v-flex lg12>
        <animeTitle1 style="padding-left:15px" :title="'GITHUB PAGES: facil, rapido, sin complicaciones'" />
    </v-flex>
    <v-flex lg12>
        <cardParagraph :textCard="textCard" :linksCard="links" :classAdd="'card01'" :fancy="true" />
    </v-flex>
     <v-flex lg12>
         <cardParagraph :textCard="textCardStep1" :classAdd="'card02'" :linksCard="linksPort" :fancy="true">
             <animeTitle2 :tClass="'step1'" :txtString="'Paso #1- crear la app'" />
         </cardParagraph>
       <window :sliceTxt="'npx create-react-app gitlab'" :txt="'npx create-react-app githubApp'" :customClass="'terminal1'" />
    </v-flex>

 
<!----->
    <v-flex lg12>
         <cardParagraph :textCard="textCardStep2" :classAdd="'card03'"  :fancy="false" >
             <animeTitle2 :tClass="'step2'" :txtString="'Paso #2- instalar algunas dependencias'"/>
         </cardParagraph>
       <window :sliceTxt="'sudo apt install hg'" :rootUser="true" :txt="'npm install gh-pages --save-dev'" :customClass="'terminal2'" />

         <cardParagraph :textCard="textCardStep3" :classAdd="'card04'"  :fancy="false"/>
          <alert :txt="packageJson" :Color="'#2196F3'" :Primary="true"/>

    </v-flex>

   <v-flex lg12>
         <cardParagraph :textCard="textCardStep4" :classAdd="'card02'"  :fancy="true">
             <animeTitle2 :tClass="'step3'" :txtString="'Adicional Para Usuarios Linux'" />
         </cardParagraph>
       <window :sliceTxt="'npx create-react-app gitlab'" :txt="'sed -i \'5i\\ \'homepage\': \'http://gitname.github.io/react-gh-pages\', \' ./package.json && sed -i \'15i\\ \'predeploy\': \'npm run build\', \' ./package.json && sed -i \'16i\\ \'deploy\': \'gh-pages -d build\', \' ./package.json'" :customClass="'terminal3'" />

        <window :sliceTxt="'npx create-react-app gitlab'" :txt="'sed -i \'15i\\ \'predeploy\': \'npm run build\', \' ./package.json && sed -i \'16i\\ \'deploy\': \'gh-pages -d build\', \' ./package.json'" :customClass="'terminal4'" />

          <window :sliceTxt="'npx create-react-app gitlab'" :txt="'sed -i \'16i\\ \'deploy\': \'gh-pages -d build\', \' ./package.json'" :customClass="'terminal5'" />
         
    </v-flex>

  <v-flex lg12>
         <cardParagraph :textCard="textCardStep5" :classAdd="'card04'"  :fancy="false" >
             <animeTitle2 :tClass="'step4'" :txtString="'Paso #3- Git remote y despliegue!'"/>
         </cardParagraph>
       <window :sliceTxt="'gitlab'" :rootUser="true" :txt="'git remote add https://githubuser.github.com/repositoriogit.git'" :customClass="'terminal6'" />
         
    </v-flex>

     <v-flex lg12>
         <cardParagraph :textCard="textCardStep5" :classAdd="'card05'"  :fancy="false" >
             <animeTitle2 :tClass="'step5'" :txtString="'Paso #3- Git push y listo!'"/>
         </cardParagraph>
 <window :sliceTxt="'npm '" :rootUser="true" :txt="'npm run deploy'" :customClass="'terminal7'" />
         <cardParagraph :textCard="textCardStep6" :classAdd="'card06'"  :fancy="false"/>
         <h2 class="text-center font-darker-grotesque"> PUEDES VER EL SITIO DESDE ESTE ENLACE!!
             <br>
             <a href="https://goth14wx.github.io/githubapp/" target="_blank">https://goth14wx.github.io/githubapp/</a>
         </h2>
    <br/>
        <customModalDialog :video="'github'"/>
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
            textCard:'Tan facil que solamente tienes que crear un solo repositorio para que se pueda realizar un CD/CI facil y rapido, es una solucion algo sencilla pero pontente, sin cargos adicionales, gracias a GITHUB',
            links:[
                {
                    to:'https://help.github.com/en/github/working-with-github-pages',
                    text:'GITHUB PAGES',
                    color:'pink'
                }
            ],
            linksPort:[
                {
                    to:'https://create-react-app.dev/docs/deployment/',
                    text:'REACT DESPLIEGUE'
                }
            ],
            textCardStep1:"En este caso utilizaremos REACT.JS para poder hacer una simple aplicación",
            textCardStep2:"Paquete necesario para poder hacer mucho mas sencilla la tarea de desplegar la app en github pages",
            textCardStep3:"ahora muy bien es solo de poder configurar el package.json",
            packageJson:`{
                    "homepage": "http://goth14wx.github.io/githubapp",
                    "scripts": {
                            ....
                            "predeploy": "npm run build",
                            "deploy": "gh-pages -d build",
                            ....
                    }
            }`,
            textCardStep4:"Esto es para poder hacer la vida mas facil a la hora de desplegar tu aplicacion",
            textCardStep5: "a un solo paso de poder obtener nuestra app de react en github es una integracion total la que se obtiene con esta herramienta de github <3",
            textCardStep6:"Listo!!, ya se encuentra nuestra app de react en github pages con integracion continua!!"
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

