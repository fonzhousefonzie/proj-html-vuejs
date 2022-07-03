<template>
    <div class="section">
        <JumboBanner
            :col-left="50"
            :col-right="50"
            :end-text="true"
            :endh6="'what are you looking for?'"
            :endh1="'Learn on your'"
            :endh1-last-word="'mobile'"
            :d-sec-endh1="true"
            :second-endh1="'anytime!'"
            :end-button="'Download Our App'"
            :img-left="background"
            :end-p="'Save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activities of enjoyment or other precious moments.'"
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
            background: require('../assets/img/home-5-image-02.png')
        }
    },
    components: { JumboBanner }
}
</script>

<style scoped lang="scss">
.section{
    padding: 3rem 0;
    background: url('../assets/img/underlay-shape-grey.svg'), url('../assets/img/maxcoach-shape-07.png');
    background-repeat: no-repeat;
    background-position: 20% bottom, 43% 80%;
    background-size: auto 80%, auto 25%;
    color: var(--gray);
}
</style>