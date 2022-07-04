<template>
  <div class="section py-5">
    <div class="container pt-5">
        <TitleAndSubtitle
            :subtitle="'people are praising maxcoach'"
            :title="'What make they'"
            :title-last-word="'love us?'"
        />
        <div class="cards-container">
            <TestimonialCard/>
        </div>
        <div class="call-to-action">
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
    components: { TitleAndSubtitle, TestimonialCard }
}
</script>

<style scoped lang="scss">
.section{
    background: var(--main-bg-light);
    .container{
        .cards-container{
            padding-top: 8rem;
            display: flex;
        }
        .call-to-action{
            padding: 2rem 0;
            position: relative;
            background: url('../assets/img/maxcoach-shape-01.png'), url('../assets/img/maxcoach-shape-02.png');
            background-repeat: no-repeat;
            background-position: 1.5rem 6rem , right bottom;
            background-size: 150px, 150px;
            .circle{
                opacity: 0.2;
                position: absolute;
                border: 8px solid var(--tortora);
                padding: 1.3rem;
                border-radius: 50%;
                left: 0;
            }
            h5{
                color: var(--main-color);
                font-weight: 600;
                span{
                    color: var(--jungle-green);
                    font-weight: normal;
                }
            }
            h2{
                color: var(--main-color);
                font-weight: 600;
                padding-bottom: 1.5rem;
            }
        }
    }
}
</style>
