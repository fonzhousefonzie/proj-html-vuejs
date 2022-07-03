<template>
    <div class="el-container">
        <h6>{{ h6 }}</h6>
        <h1>{{ h1 }} <span>{{ h1LastWord }}</span></h1>
        <p :class="{'colored' : coloredText}">{{ p }}</p>
        <ul :class="{ 'd-none': !list }">
            <li v-for="li in listItems" :key="li"><i class="fa fa-solid fa-check me-3"></i>{{li}}</li>
        </ul>
        <button class="primary-btn"><i class="me-2" :class="buttonIconClass"></i>{{button}}</button>
    </div>
</template>

<script>
export default {
    props: {
        h6: String,
        h1: String,
        h1LastWord: String,
        p: String,
        coloredText: Boolean,
        list: Boolean,
        listItems: Array,
        button: String,
        buttonIconClass: String
    }
}
</script>

<style lang="scss" scoped>
.el-container{
    padding: 0 4rem;

    h6, h1, p, ul{
        margin: 2rem 0;
    }
}
.colored{
    color: var(--main-color-light);
    font-weight: bold;
}
</style>