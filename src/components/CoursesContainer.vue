<template>
    <div class="section py-5">
        <div class="container py-5">
            <TitleAndSubtitle :title="'Latest Featured'" :title-last-word="'Courses'"
                :subtitle="`choose where you'd like to begin`" />
            <div class="cards-container d-flex flex-wrap justify-content-between pt-4 gap-4">
                <CourseCard v-for="card in cards" :key="card.courseTitle"
                :img-url="card.imgUrl"
                :price="card.price"
                :is-price-number="card.isPriceNumber"
                :teacher-img-url="card.teacherImgUrl"
                :teacher-name="card.teacherName"
                :course-title="card.courseTitle"
                :lessons-num="card.lessonsNum"
                :students-num="card.studentsNum"
                />
            </div>
            <button class="primary-btn mt-5">View all courses <i class="fa fa-solid fa-arrow-right"></i></button>
        </div>
    </div>
</template>

<script>
import TitleAndSubtitle from './TitleAndSubtitle.vue';
import CourseCard from './CourseCard.vue';
export default {
    data() {
        return {
            cards: [
                {
                    imgUrl: require("../assets/img/course-02-480x298.jpg"),
                    price: "40",
                    isPriceNumber: true,
                    teacherImgUrl: require("../assets/img/73ee246daf47502812ccefc84bf02898 (1).jpeg"),
                    teacherName: "Blanche Fields",
                    courseTitle: "Learning to Write as a Professional Author",
                    lessonsNum: "20",
                    studentsNum: "50"
                },
                {
                    imgUrl: require("../assets/img/stock-full-hd-03-480x298.jpg"),
                    price: "Free",
                    isPriceNumber: false,
                    teacherImgUrl: require("../assets/img/d0d504142acfde820eef2f11feea6253 (1).jpeg"),
                    teacherName: "Maggie Strickland",
                    courseTitle: "Customer-centric Info-Tech Strategies",
                    lessonsNum: "24",
                    studentsNum: "769"
                },
                {
                    imgUrl: require("../assets/img/stock-full-hd-04-480x298.jpg"),
                    price: "19",
                    isPriceNumber: true,
                    teacherImgUrl: require("../assets/img/d0d504142acfde820eef2f11feea6253 (1).jpeg"),
                    teacherName: "Maggie Strickland",
                    courseTitle: "Open Programming Courses for Everyone: Python",
                    lessonsNum: "17",
                    studentsNum: "62"
                },
                {
                    imgUrl: require("../assets/img/stock-full-hd-06-480x298.jpg"),
                    price: "26",
                    isPriceNumber: true,
                    teacherImgUrl: require("../assets/img/73ee246daf47502812ccefc84bf02898 (1).jpeg"),
                    teacherName: "Blanche Fields",
                    courseTitle: "Academic Listening and Note-taking",
                    lessonsNum: "14",
                    studentsNum: "67"
                },
                {
                    imgUrl: require("../assets/img/course-featured-image-01-480x298.jpg"),
                    price: "39",
                    isPriceNumber: true,
                    teacherImgUrl: require("../assets/img/73ee246daf47502812ccefc84bf02898 (1).jpeg"),
                    teacherName: "Blanche Fields",
                    courseTitle: "Master jQuery in a Short Period of Time",
                    lessonsNum: "6",
                    studentsNum: "51"
                },
                {
                    imgUrl: require("../assets/img/stock-full-hd-05-480x298.jpg"),
                    price: "59",
                    isPriceNumber: true,
                    teacherImgUrl: require("../assets/img/73ee246daf47502812ccefc84bf02898 (1).jpeg"),
                    teacherName: "Blanche Fields",
                    courseTitle: "Introduction to Javascript for Beginners",
                    lessonsNum: "14",
                    studentsNum: "76"
                },
            ]
        }
    },
    components: { TitleAndSubtitle, CourseCard }
}
</script>

<style scoped lang="scss">
.section {
    background: var(--main-bg-light);
    border-radius: 0% 0% 100% 100% / 0% 0% 10% 10%;
    .cards-container>*{
        max-width: 32%;
    }
}
</style>