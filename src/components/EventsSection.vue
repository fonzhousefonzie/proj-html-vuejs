<template>
    <div class="section mt-5">
        <div class="background py-5">
            <div class="container py-5">
                <TitleAndSubtitle :title="'Upcoming'" :title-last-word="'Events'" :subtitle="'get in contact now'" />
                <div class="events-container row row-cols-2">
                    <div class="col p-3" v-for="event in events" :key="event.event">
                    <EventCard :location="event.location"
                        :event="event.event" :day="event.day" :month="event.month" />
                    </div>
                </div>
                <p class="cta">Excited about our event? <a href="#">View all events <i class="fa fa-solid fa-arrow-right"></i></a></p>
            </div>
        </div>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';
import EventCard from './EventCard.vue';
export default {
    data() {
        return {
            events: [
                {
                    location: "Texas, US",
                    event: "Storytelling Workshop",
                    day: 22,
                    month: "nov",
                },
                {
                    location: "New York, US",
                    event: "Painting Art Contest 2020",
                    day: 10,
                    month: "oct",
                },
                {
                    location: "Hamburg, Germany",
                    event: "International Art Fair 2020",
                    day: 23,
                    month: "nov",
                },
                {
                    location: "Illinois, US",
                    event: "Street Performance: Call for Artist",
                    day: 15,
                    month: "dec",
                },
                {
                    location: "Illinois, US",
                    event: "Consumer Food Safety Education Conference",
                    day: 22,
                    month: "jul",
                },
                {
                    location: "Dubai",
                    event: "How meditation improve our mental health?",
                    day: 12,
                    month: "aug",
                },
            ]
        }
    },
    components: { TitleAndSubtitle, EventCard }
}
</script>

<style scoped lang="scss">
.section {
    background: var(--main-bg-light);

    .background {
        background: var(--white);
        border-radius: 0% 0% 60% 0% / 0% 0% 30% 0%;
        .cta{
            padding: 2rem 0;
            color: var(--main-color-light);
            font-weight: 600;
            a{
                color: var(--jungle-green);
                border-bottom: 0.5px solid var(--jungle-green);
                &:hover{
                    color: var(--main-color);
                    border-color: var(--main-color)
                }
            }
        }
    }
}
</style>
