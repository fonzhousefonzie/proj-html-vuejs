<template>
    <div class="py-4">
        <h6 class="text-uppercase pb-2" :class="{'d-none' : noSub}">{{subtitle + ' '}} <span>{{subtitleLastWord}}</span></h6>
        <h1>{{title + ' '}}<span :class="{'text-uppercase' : textUp}">{{titleLastWord}}</span></h1>
        <h1 :class="{'d-none' : !displaySecondTitle}">{{secondTitle}}</h1>
    </div>
</template>

<script>

export default {
    props:{
        noSub: Boolean,
        subtitle: String,
        subtitleLastWord: String,
        title: String,
        displaySecondTitle: Boolean,
        secondTitle:String,
        titleLastWord: String,
        textUp: Boolean
    }
}
</script>

<style lang="scss" scoped>
    h6{
        color: var(--gray);
        letter-spacing: 1px;
        span{
            font-weight: bold;
        }
    }

    h1 span{
        font-weight: normal;
        color: var(--jungle-green);
    }
</style>