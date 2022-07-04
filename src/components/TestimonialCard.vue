<template>
    <div class="testimonial-card">
        <div class="relative">
            <img src="../assets/img/testimonial-avata-01.jpg" alt="">
            <p class="main-text">I am free to learn at my own pace,
                follow my own schedule and choose
                the subject I like. Great study portal
                for people like me.</p>
            <h6>Mina Hollace</h6>
            <p><span>/ </span>Freelancer</p>
        </div>
    </div>
</template>

<script>
export default {
}
</script>

<style scoped lang="scss">
.testimonial-card {
    width: 32%;
    padding: 0 1rem;
    background: var(--white);
    border-radius: 0.5rem;
    box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.1);
    height: 410px;

    .relative {
        position: relative;
        bottom: 3rem;

        img {
            position: relative;
            bottom: 3rem;
            border-radius: 50%;
            width: 200px;
        }

        .main-text {
            margin-top: -1.5rem;
            font-size: 1.2rem;
            color: var(--main-color);
        }

        h6 {
            text-transform: uppercase;
            font-weight: 600;
            padding-top: 2rem;
        }

        p {
            padding-top: 0.5rem;
        }
    }
}
</style>