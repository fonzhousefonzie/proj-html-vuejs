<template>
    <div class="section">
        <div class="container">
            <TitleAndSubtitle :title="'Build Your Dream'" :title-last-word="'Today'" :text-up="true" :subtitle="'start learning coding languages'"/>
            <div class="cards-container d-flex">
                <SimpleCard v-for="card in cards" :key="card.title"
                    :img-url="require('../assets/img/' + card.img)"
                    :title="card.title"
                    :text="card.text"
                    :button="card.button"
                />
            </div>
        </div>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';
import SimpleCard from './SimpleCard.vue';
export default {
    data(){
        return{
            cards:[
                {
                    img: "home-5-image-box-01.png",
                    title: "Idea Discussion",
                    text: "Get teamed up with the specialists who work and teach coding for years at famous universities.",
                    button: "Start now"
                },
                {
                    img: "home-5-image-box-02.png",
                    title: "Web Development",
                    text: "Learn to start building a webpage from scratch. You decide your ownpace, course and speed.",
                    button: "Start now"
                },
                {
                    img: "home-5-image-box-03.png",
                    title: "System Administration",
                    text: "Learners are encouraged to study the mechanism and structure of system administration.",
                    button: "Start now"
                },
                {
                    img: "home-5-image-box-04.png",
                    title: "Graphic Design",
                    text: "Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.",
                    button: "Start now"
                }
            ]
        }
    },
    components: { TitleAndSubtitle, SimpleCard }
}
</script>

<style lang="scss" scoped>
    .section{
        background: var(--main-bg-light);
    }
</style>