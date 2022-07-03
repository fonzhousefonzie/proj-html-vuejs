<template>
    <div>
        <h1>{{counter}}</h1>
        <h6>{{title}}</h6>
    </div>
</template>

<script>
export default {
    props:{
        counter: String,
        title: String
    }
}
</script>

<style lang="scss" scoped>
    h1{
        font-weight: 800;
        color: var(--jungle-green);
    }

    h6{
        text-transform: uppercase;
        font-weight: 600;
        color: var(--main-color);
    }
</style>