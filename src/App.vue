<template>
  <div id="app">
    <TheHeader />
    <JumboSection />
    <CardsBanner />
    <SecondJumbo />
    <CounterBanner />
    <CoursesContainer />
    <BannerOne />
    <BannerTwo />
    <EventsSection />
    <TestimonialsSection />
    <TheFooter />
    <a href="#" class="primary-btn" id="upBtn"><i class="fa fa-solid fa-arrow-up"></i></a>
    <div id="sideMenu">
      <i class="fa-solid fa-ruler-combined">
        <div class="side-div">
          <ul class="list-unstyled">
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
          </ul>
        </div>
      </i>
      <i class="fa-regular fa-life-ring">
        <div class="side-div">
          <ul class="list-unstyled">
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
          </ul>
        </div>
      </i>
      <i class="fa-solid fa-book">
        <div class="side-div">
          <ul class="list-unstyled">
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
          </ul>
        </div>
      </i>
      <i class="fa-solid fa-cart-shopping">
        <div class="side-div">
          <ul class="list-unstyled">
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
            <li>a side link</li>
          </ul>
        </div>
      </i>
    </div>
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
import TestimonialsSection from './components/TestimonialsSection.vue';

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
    EventsSection,
    TestimonialsSection
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
  --white: #fefefe;
  --light-blue: #b6b8d1;
  --blue: #01afc8;
  --light-blue: #b6b8d1;
  --gray: #959999;
  --jungle-green: #22ad96;
  --dark-green: #458d76;
  --orange: #f29518;
  --tortora: #a08778;
  --piza: #fb9301;
  --black: #0e0e0e;
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

  &:hover {
    color: var(--main-color-light);
  }
}

h1 {
  font-weight: 600;
  color: var(--main-color);
}

h5 {
  font-size: 1.4rem;
}

h6 {
  font-size: 1.1rem;
}

button {
  border: none;
  outline: none;
  padding: 0.7rem 2rem;
  border-radius: 0.3rem;
}

#upBtn {
  position: fixed;
  display: flex;
  align-items: center;
  z-index: 10;
  right: 2rem;
  bottom: 2rem;
  border-radius: 50%;
  padding: 0 1.5rem;
  aspect-ratio: 1 / 1;
  font-size: 1.5rem;

  &:hover {
    color: var(--white);
  }
}

.primary-btn {
  background: var(--jungle-green);
  color: var(--white);
  font-weight: 600;

  &:hover {
    background: var(--main-color);
  }
}

.primary-btn.large {
  padding: 0.7rem 3.5rem;
}

.primary-btn.small {
  padding: 0.3rem 2.5rem;
  font-size: 0.8rem;
}

.secondary-btn {
  padding: 0.7rem 4rem;
  background: none;
  color: var(--main-color-light);
  font-weight: 600;
  font-size: 0.9rem;

  &:hover {
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

.col-40 {
  width: 40%;
}

.col-50 {
  width: 50%;
}

.col-60 {
  width: 60%;
}

#sideMenu {
  position: fixed;
  right: 0px;
  top: 180px;
  display: flex;
  flex-direction: column;
  background: var(--white);
  border-radius: 0.5rem 0 0 0.5rem;
  box-shadow: 0 0 2rem rgba(0, 0, 0, 0.1);

  i {
    padding: 0.7rem;
    display: flex;

    &:hover {
      color: var(--main-color-light);
      .side-div{
        display: block;
      }
    }

    .side-div {
      display: none;
      left: 100%;
      top: 0;
      width: 150px;
      li{
        cursor: pointer;
        font-family: 'Poppins', sans-serif;
        font-weight: normal;
        color: var(--main-color);
        text-transform: capitalize;
        padding: 0.5rem 0;
        &:hover{
          color: var(--main-color-light);
        }
      }
    }
  }
}
</style>
