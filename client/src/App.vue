<script setup>
  // новые картинки
  // карта в contact us
  // реализовать таблицы customer(), gallery+events(id, date, title, information, img), 
  // menu+slider-food(id, category, title, img, price), reservation(), blog(id, title, img, author, information), 
  // review(id, review, img, name) 
  // создать компонент модального окна для gallery & events, menu-product & slider-food, reservation, review
  // реализовать локальное хранилище (замена его в vue) или систему кэша для корзины (basket) или все таки таблицу в бд.
  
  import Preloader from './components/preloader.vue';
  import Header from './components/header.vue';
  import Home from './components/home.vue';
  import About from './components/about.vue';
  import SpecialDish from './components/special-dish.vue';
  import DealEvents from './components/deal-events.vue';
  import Menu from './components/menu.vue';
  import OurDeliciousFood from './components/our-delicious-food.vue';
  import Reservation from './components/reservation.vue';
  import OurBlogs from './components/our-blogs.vue';
  import CustomersReview from './components/customers-review.vue';
  import ContactUs from './components/contact-us.vue';
  import Footer from './components/footer.vue';
</script>

<template>
  <Preloader />
  <Header />
  <Home />
  <About />
  <SpecialDish />
  <DealEvents />
  <Menu />
  <OurDeliciousFood />
  <Reservation />
  <OurBlogs />
  <CustomersReview />
  <ContactUs />
  <Footer />

</template>

<style scoped lang="scss">
  @import './styles.scss';
</style> 