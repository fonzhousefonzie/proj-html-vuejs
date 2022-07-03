<template>
    <div class="simple-card">
        <img :src="imgUrl" alt="">
        <h6 class="fw-bold">{{title}}</h6>
        <p>{{text}}</p>
        <button class="secondary-btn">{{button}}<i class="fa fa-solid fa-arrow-right ps-3"></i></button>
    </div>
</template>

<script>
export default {
    props:{
        imgUrl: String,
        title: String,
        text: String,
        button: String
    }
}
</script>

<style lang="scss" scoped>
.simple-card{
    padding: 0.5rem;
    img{
        max-width: 100%;
        padding-bottom: 1.5rem;
    }
    h6{
        padding: 0.5rem 0;
    }
}
</style>