<template>
    <div class="testimonial-card">
        <div class="relative">
            <img :src="imgUrl" alt="">
            <p class="main-text">{{text}}</p>
            <h6>{{testimonialName}}</h6>
            <p><span>/ </span>{{job}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        imgUrl: String,
        text: String,
        testimonialName: String,
        job: String
    }
}
</script>

<style scoped lang="scss">
.testimonial-card {
    width: 30.4%;
    flex-shrink: 0;
    padding: 0 2rem;
    background: var(--white);
    border-radius: 0.5rem;
    box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.1);
    height: 350px;

    .relative {
        position: relative;
        bottom: 1.5rem;

        img {
            position: relative;
            bottom: 3rem;
            border-radius: 50%;
            width: 150px;
        }

        .main-text {
            margin-top: -1.5rem;
            font-size: 1rem;
            font-weight: 500;
            color: var(--main-color);
        }

        h6 {
            text-transform: uppercase;
            font-weight: 600;
            font-size: 1rem;
            padding-top: 2rem;
        }

        p {
            padding-top: 0.5rem;
            font-size: 0.8rem;
        }
    }
}
</style>