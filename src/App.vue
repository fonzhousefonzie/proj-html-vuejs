<template>
  <div id="app">
    <TheHeader />
    <JumboSection/>
    <CardsBanner/>
    <SecondJumbo/>
    <CounterBanner/>
    <CoursesContainer/>
    <BannerOne/>
    <BannerTwo/>
    <EventsSection/>
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';
import CardsBanner from './components/CardsBanner.vue';
import JumboSection from './components/JumboSection.vue';
import SecondJumbo from './components/SecondJumbo.vue';
import CounterBanner from './components/CounterBanner.vue';
import CoursesContainer from './components/CoursesContainer.vue';
import BannerOne from './components/BannerOne.vue';
import BannerTwo from './components/BannerTwo.vue';
import EventsSection from './components/EventsSection.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    TheFooter,
    CardsBanner,
    JumboSection,
    SecondJumbo,
    CounterBanner,
    CoursesContainer,
    BannerOne,
    BannerTwo,
    EventsSection
}
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

:root {
  --main-bg: #f0efef;
  --main-bg-light: #f9f9f9;
  --main-color: #513e5e;
  --main-color-rgb: 81, 62, 94;
  --main-color-light: rgba(81, 62, 94, 0.5);
  --green: #22ad96;
  --white: #fefefe;
  --light-blue: #b6b8d1;
  --blue: #01afc8;
  --light-blue: #b6b8d1;
  --gray: #959999;
  --jungle-green: #22ad96;
  --dark-green: #458d76;
  --orange: #f29518;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: var(--white);
}

ul {
  list-style: none;
  padding: 0;
}

a {
  text-decoration: none;
  color: inherit;
}

h1{
  font-weight: 600;
  color: var(--main-color);
}

h5{
  font-size: 1.4rem;
}

h6 {
  font-size: 1.1rem;
}

button{
  border: none;
  outline: none;
  padding: 0.7rem 2rem;
  border-radius: 0.3rem;
}

.primary-btn{
  background: var(--jungle-green);
  color: white;
  font-weight: 600;
  &:hover{
    background: var(--main-color);
  }
}

.primary-btn.small{
  padding: 0.3rem 2.5rem;
  font-size: 0.8rem;
}

.secondary-btn{
  padding: 0.7rem 4rem;
  background: none;
  color: var(--main-color-light);
  font-weight: 600;
  font-size: 0.9rem;
  &:hover{
    background: var(--main-bg);
    color: var(--jungle-green);
  }
}

input[type="text"] {
  border: none;
  outline: none;
  padding: 0.7rem 1rem;
  border-radius: 0.3rem;
}

.col-40{
  width: 40%;
}

.col-50 {
  width: 50%;
}

.col-60{
  width: 60%;
}
</style>
