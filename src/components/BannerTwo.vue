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
                <div class="circle"></div>
    </div>
</template>

<script>
import JumboBanner from './JumboBanner.vue';
export default {
    data(){
        return{
            background: require('../assets/img/home-5-image-02.png')
        }
    },
    components: { JumboBanner }
}
</script>

<style scoped lang="scss">
.section{
    position: relative;
    padding: 3rem 0;
    background: url('../assets/img/underlay-shape-grey.svg'), url('../assets/img/maxcoach-shape-07.png'), url('../assets/img/maxcoach-shape-01.png');
    background-repeat: no-repeat;
    background-position: 20% bottom, 43% 80%, 12.5% 48%;
    background-size: auto 80%, auto 25%, auto 5%;
    color: var(--gray);
    .circle {
                opacity: 0.2;
                position: absolute;
                border: 8px solid var(--piza);
                padding: 1.3rem;
                border-radius: 50%;
                left: 45%;
                top: 15%;
            }
}
</style>