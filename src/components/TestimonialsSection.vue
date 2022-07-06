<template>
    <div class="section py-5">
        <div class="container pt-5">
            <TitleAndSubtitle :subtitle="'people are praising maxcoach'" :title="'What make they'"
                :title-last-word="'love us?'" />
            <div class="cards-container" ref="cards">
                <TestimonialCard v-for="testimonial in testimonials" :key="testimonial.name" :img-url="testimonial.img"
                    :text="testimonial.text" :testimonial-name="testimonial.name" :job="testimonial.job" />
            </div>
            <div class="dots-container pb-5 d-flex justify-content-center align-items-center">
                <div v-for="(testimonial, i) in testimonials" :key="i" 
                :id="'dot' + i" class="dot" :class="{'active' : i === active}"></div>
            </div>
            <div class="call-to-action mb-4">
                <div class="circle"></div>
                <h5>Start today for getting <span>Online Certification</span></h5>
                <h2>You can be your own guiding star with our help!</h2>
                <button class="primary-btn large">Get started now</button>
            </div>
        </div>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';
import TestimonialCard from './TestimonialCard.vue';
export default {
    data() {
        return {
            testimonials: [
                {
                    img: require('../assets/img/testimonial-avata-02.jpg'),
                    text: "I am free to learn at my own pace, follow my own schedule and choose the subject I like.Great study portal for people like me.",
                    name: "Mina Hollace",
                    job: "Freelancer"
                },
                {
                    img: require('../assets/img/testimonial-avata-04.jpg'),
                    text: "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
                    name: "Madley Pondor",
                    job: "IT Specialist"
                },
                {
                    img: require('../assets/img/testimonial-avata-01.jpg'),
                    text: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
                    name: "Luvic Dubble",
                    job: "Private Tutor"
                },
                {
                    img: require('../assets/img/testimonial-avata-03.jpg'),
                    text: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Natus quia dicta corrupti nesciunt eum pariatur cupiditate optio quis.",
                    name: "John Doe",
                    job: "Web Developer"
                },
            ],
            active: 0
        }
    },
    methods: {
        swipe() {
            const th = this;
            setInterval(function () {
                //cards
                const cards = th.$refs.cards;
                cards.scrollBy({
                    left: 10000,
                    behavior: 'smooth'
                });
                setTimeout(function(){
                const element = th.testimonials[0];
                th.testimonials.splice(0, 1);
                th.testimonials.splice(3, 0, element);
                cards.scrollBy({
                    left: -10000,
                    behavior: 'instant'
                })
                }, 500)
                //dots
                if(th.active < th.testimonials.length - 1){
                    th.active = th.active + 1
                } else if(th.active === th.testimonials.length - 1){
                    th.active = 0
                }
            }, 10000)
        }
    },
    mounted() {
        this.swipe()
    },
    components: { TitleAndSubtitle, TestimonialCard }
}
</script>

<style scoped lang="scss">
.section {
    background: var(--main-bg-light);

    .container {
        .cards-container {
            padding: 8rem 2rem 3rem;
            display: flex;
            flex-wrap: nowrap;
            gap: 3.5rem;
            overflow-x: hidden;
        }

        .dots-container {
            min-height: 100px;
            .dot {
                border: 4px solid var(--main-color-light);
                border-radius: 50%;
                margin: 0.7rem;
                transition: 500ms ease;
            }

            .active {
                border: 6px solid var(--main-color)
            }
        }

        .call-to-action {
            padding: 2rem 0;
            position: relative;
            background: url('../assets/img/maxcoach-shape-01.png'), url('../assets/img/maxcoach-shape-02.png');
            background-repeat: no-repeat;
            background-position: 1.5rem 6rem, right bottom;
            background-size: 150px, 150px;

            .circle {
                opacity: 0.2;
                position: absolute;
                border: 8px solid var(--tortora);
                padding: 1.3rem;
                border-radius: 50%;
                left: 0;
            }

            h5 {
                color: var(--main-color);
                font-weight: 600;

                span {
                    color: var(--jungle-green);
                    font-weight: normal;
                }
            }

            h2 {
                color: var(--main-color);
                font-weight: 600;
                padding-bottom: 1.5rem;
            }
        }
    }
}
</style>
