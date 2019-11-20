<template>
<v-container>
     <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
    <v-col class="text-center">
         <animeTitle1 style="padding-left:15px" :title="'NETLIFY, MAS FACIL IMPOSIBLE'" />
    </v-col>
 </v-row>
 <v-row>
       <v-col>
        <iframe width="100%" height="400px"  src="https://www.youtube.com/embed/152-yYIMkho" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </v-col>
 </v-row>
 <v-row>
     <v-col>
          <h2 class="text-center font-darker-grotesque"> ¿EL ENLACE AL SITIO WEB?
             <br>
             <h3>ESTAS EN EL</h3>
         </h2>
     </v-col>
 </v-row>
</v-container>
</template>
<script>
import animeTitle1 from '@/components/shared/customTitles/animeTitle1';
export default {
    data(){
        return{

        }
    },
    components:{
        animeTitle1
    }
}
</script>