<template>
    <div class="section py-5">
        <div class="container d-flex justify-content-around py-3">
            <CounterCard v-for="card in counters" :key="card.text" 
                :counter="card.number"
                :title="card.text"
            />
        </div>
    </div>
</template>

<script>
import CounterCard from './CounterCard.vue';
export default {
    data() {
        return {
            counters: [
                {
                    number: "1.926",
                    text: "finished sessions"
                },
                {
                    number: "3.092+",
                    text: "enrolled learners"
                },
                {
                    number: "200",
                    text: "online instructors"
                },
                {
                    number: "100%",
                    text: "satisfaction rate"
                }
            ]
        }
    },
    components: { CounterCard }
}
</script>

<style lang="scss" scoped>
.section{
    background: var(--main-bg);
}
</style>