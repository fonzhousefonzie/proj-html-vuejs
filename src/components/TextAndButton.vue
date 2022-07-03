<template>
    <div class="el-container">
        <TitleAndSubtitle
            :subtitle="h6"
            :title="h1"
            :title-last-word="h1LastWord"
        :noSub="noSub"
        :subtitleLastWord="h6LastWord"
        :displaySecondTitle="displaysecondh1"
        :secondTitle="secondh1"
        :textUp="textUp"
        />
        <p :class="{'colored' : coloredText, 'd-none' : dontDisplayP}">{{ p }}</p>
        <ul :class="{ 'd-none': !list }">
            <li v-for="li in listItems" :key="li"><i class="fa fa-solid fa-check me-3"></i>{{li}}</li>
        </ul>
        <button class="primary-btn"><i class="me-2" :class="buttonIconClass"></i>{{button}}</button>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';
export default {
    props: {
        noSub: Boolean,
        h6: String,
        h6LastWord: String,
        textUp: Boolean,
        h1: String,
        h1LastWord: String,
        displaysecondh1: Boolean,
        secondh1: String,
        dontDisplayP: Boolean,
        p: String,
        coloredText: Boolean,
        list: Boolean,
        listItems: Array,
        button: String,
        buttonIconClass: String
    },
    components: { TitleAndSubtitle }
}
</script>

<style lang="scss" scoped>
.el-container{
    padding: 0 3rem;
    p{
        padding-bottom: 1.5rem;
    }

    li{
        color: var(--gray);
        padding-bottom: 1rem;
    }
}
.colored{
    color: var(--main-color-light);
    font-weight: 600;
}
</style>