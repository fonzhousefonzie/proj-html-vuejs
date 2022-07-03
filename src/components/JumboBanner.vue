<template>
    <div class="container d-flex text-start">
        <div :class="{'col-50' : colLeft===50, 'col-40' : colLeft===40, 'col-60' : colLeft===60, 'img-small' : imgSmall}" :style="{ backgroundImage: 'url(' + imgLeft + ')' }">
            <TextAndButton :class="{ 'd-none': !startText }" :no-sub="noSubStart" :h6="starth6" :h1="starth1" :h1-last-word="starth1LastWord" :displaysecondh1="dSecStarth1" :secondh1="secondStarth1"
                :p="startP" :colored-text="true" :list="startList" :list-items="startListItems" :button="startButton" :dont-display-p="dontDisplayStartText"
                :button-icon-class="startBtnIcon" />
        </div>
        <div :class="{'col-50' : colRight===50, 'col-40' : colRight===40, 'col-60' : colRight===60, 'img-small' : imgSmall}" :style="{ backgroundImage: 'url(' + imgRight + ')' }">
            <TextAndButton :class="{ 'd-none': !endText }" :no-sub="noSubEnd" :h6="endh6" :h1="endh1" :h1-last-word="endh1LastWord" :displaysecondh1="dSecEndh1" :secondh1="secondEndh1"
                :p="endP" :list="endList" :list-items="endListItems" :button="endButton" :dont-display-p="dontDisplayEndText"
                :button-icon-class="endBtnIcon" />
        </div>
    </div>
</template>

<script>
import TextAndButton from './TextAndButton.vue'

export default {
    props: {
        dSecStarth1: Boolean,
        secondStarth1: String,
        dSecEndh1: Boolean,
        secondEndh1: String,
        noSubStart: Boolean,
        noSubEnd: Boolean,
        colLeft: Number,
        colRight: Number,
        imgLeft: String,
        imgRight: String,
        imgSmall:Boolean,
        dontDisplayStartText: Boolean,
        startText: Boolean,
        dontDisplayEndText: Boolean,
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
.col-50, .col-40, .col-60 {
    padding: 4rem;
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
}

.img-small{
    background-position: bottom;
    background-size: auto 90%;
}
</style>