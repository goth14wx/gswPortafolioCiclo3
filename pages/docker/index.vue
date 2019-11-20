<template>
    <v-container>
        <v-row>
            <v-col class="text-center">
                <animeTitle1 style="padding-left:15px" :title="'DOCKER ES ASOMBROSO'" />
            </v-col>
        </v-row>
        <v-row>
            <v-col>
                <iframe src="//slides.com/goth14wx/deck-28fca4/embed" width="100%" height="500px" scrolling="no" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
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