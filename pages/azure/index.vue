<template>
    <v-container>
        <v-row>
            <v-col class="text-center">
                <animeTitle1 style="padding-left:15px" :title="'AZURE NO FUNCIONA'" />
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <cardParagraph :textCard="texto" :classAdd="'card06'"  :fancy="false"/>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import animeTitle1 from '@/components/shared/customTitles/animeTitle1';
import cardParagraph from '@/components/shared/cardParagraph';
export default {
    data(){
        return{
            texto:"Por mas que intente azure no funcionaba pero puedo dejar el proceso que segui "
        }
    },
    components:{
        animeTitle1,
        cardParagraph,
        
    }
}
</script>