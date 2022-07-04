<template>
    <div class="section pt-5">
        <div class="container text-start d-flex">
            <div class="col-50 img"></div>
            <div class="col-50 p-4">
                <TitleAndSubtitle :title="'Construct A'" :title-last-word="'Stunning'" :display-second-title="true"
                    :second-title="'Career Perspective'" :subtitle="'dream with'" :subtitle-last-word="'maxcoach'" />
                <div class="dropdown-container">
                    <div class="dropdown" v-for="object in dropdowns" :key="object.title" @click="showText(object)">
                        <h6 class="d-flex justify-content-between" :class="{ 'd-none': object.show }">{{ object.title }}
                            <i class="fa-solid fa-circle-plus"></i></h6>
                        <div class="show" :class="{ 'd-none': !object.show }">
                            <h6 class="d-flex justify-content-between">{{ object.title }} <i
                                    class="fa-solid fa-circle-minus"></i></h6>
                            <p>{{ object.content }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';

export default {
    data() {
        return {
            dropdowns: [
                {
                    show: true,
                    title: "Multiple Platforms Supported for Teaching & Studying",
                    content: "MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access our knowledge base from any device."
                },
                {
                    show: false,
                    title: "Multiple Course Participation at the Same Time",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt atque placeat recusandae assumenda, quasi odio et, libero nobis nostrum accusamus."
                },
                {
                    show: false,
                    title: "Track Study Progress & eliver Prompt Feedback",
                    content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt atque placeat recusandae assumenda, quasi odio et, libero nobis nostrum accusamus."
                }
            ],
            image: require('../assets/img/about-us-03-image-01.png')
        }
    },
    components: { TitleAndSubtitle },
    methods: {
        showText(object) {
            for (let i = 0; i < this.dropdowns.length; i++) {
                this.dropdowns[i].show = false;
            }
            object.show = true;
        }
    }
}
</script>

<style lang="scss" scoped>
.section {
    background: var(--main-bg-light);
}

.container {
    min-height: 750px;
}

.img {
    background: url('../assets/img/about-us-03-image-01.png'), url('../assets/img/underlay-shape-lilla.svg');
    background-position: center, left center;
    background-size: 60%, 55%;
    background-repeat: no-repeat;
}

.dropdown-container {
    padding-top: 1rem;
}

.dropdown {
    background: var(--white);
    margin-bottom: 2rem;
    border-radius: 0.5rem;
    box-shadow: 0 0.5rem 2rem rgba(0, 0, 0, 0.1);
    cursor: pointer;
    overflow: hidden;
    position: relative;

    >h6 {
        color: var(--gray);
        font-weight: bold;
        padding: 1rem 1rem 1.2rem;
        margin: 0;

        &:hover {
            background: var(--main-bg-light);
        }
    }

    .show {
        h6 {
            background: var(--jungle-green);
            padding: 1rem;
            color: var(--white);
            font-weight: bold;
        }

        p {
            padding: 1rem;
            color: var(--gray);
        }
    }
}
</style>