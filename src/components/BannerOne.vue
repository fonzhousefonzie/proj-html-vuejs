<template>
    <div class="section">
        <JumboBanner
            :col-left="50"
            :col-right="50"
            :start-text="true"
            :starth6="'why hesitate to register?'"
            :starth1="'Learn At Your Own'"
            :starth1-last-word="'Pace'"
            :start-list="true"
            :start-list-items="listItems"
            :dont-display-start-text="true"
            :start-button="'Get started for free'"
            :img-right="background"
            :img-small="true"
        />
    </div>
</template>

<script>
import JumboBanner from './JumboBanner.vue';
export default {
    data(){
        return{
            listItems:[
                "Select & customize courses to your preferences",
                "Change the tutor and make arrangements",
                "Participate in events to join others",
                "Get the desired certificate delivered at house"
            ],
            background: require('../assets/img/home-5-image-01.png')
        }
    },
    components: { JumboBanner }
}
</script>

<style scoped lang="scss">
.section{
    padding: 3rem 0;
    background: url('../assets/img/underlay-shape-grey.svg'), url('../assets/img/maxcoach-shape-05.png');
    background-repeat: no-repeat;
    background-position: 65% bottom, 80% 80%;
    background-size: auto 65%, auto 25%;
}
</style>