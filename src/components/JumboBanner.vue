<template>
    <div class="container d-flex text-start">
        <div class="col-50" :style="{ backgroundImage: 'url(' + imgLeft + ')' }">
            <TextAndButton :class="{ 'd-none': !startText }" :h6="starth6" :h1="starth1" :h1-last-word="starth1LastWord"
                :p="startP" :colored-text="true" :list="startList" :list-items="startListItems" :button="startButton"
                :button-icon-class="startBtnIcon" />
        </div>
        <div class="col-50" :style="{ backgroundImage: 'url(' + imgRight + ')' }">
            <TextAndButton :class="{ 'd-none': !endText }" :h6="endh6" :h1="endh1" :h1-last-word="endh1LastWord"
                :p="endP" :list="endList" :list-items="endListItems" :button="endButton"
                :button-icon-class="endBtnIcon" />
        </div>
    </div>
</template>

<script>
import TextAndButton from './TextAndButton.vue'

export default {
    props: {
        imgLeft: String,
        imgRight: String,
        startText: Boolean,
        endText: Boolean,
        starth6: String,
        starth1: String,
        starth1LastWord: String,
        startP: String,
        startList: Boolean,
        startListItems: Array,
        startButton: String,
        startBtnIcon: String,
        endh6: String,
        endh1: String,
        endh1LastWord: String,
        endP: String,
        endList: Boolean,
        endListItems: Array,
        endButton: String,
        endBtnIcon: String
    },
    components: { TextAndButton }
}
</script>

<style lang="scss" scoped>
.col-50 {
    padding: 4rem;
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
}
</style>