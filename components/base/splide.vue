<template>
    <div class="slider-container">
      <Splide 
        :options="options" 
        aria-label="Каталог продукции"
        ref="splide"
      >
        <SplideSlide v-for="(slide, index) in slides" :key="index">
          <div class="slide-content">
            <h3>{{ slide.title }}</h3>
            <p>{{ slide.description }}</p>
            <img :src="slide.image" :alt="slide.title" class="slide-image">
          </div>
        </SplideSlide>
      </Splide>
  
      <ul class="splide__pagination custom-pagination"></ul>
    </div>
  </template>
  
  <script setup>
    import { Splide, SplideSlide } from '@splidejs/vue-splide';
    import '@splidejs/splide/css/sea-green';
    import { ref } from 'vue';

    import banner_pig from '~/assets/images/banner_pig.png'
    import banner_chicken from '~/assets/images/banner_chicken.png'
    import banner_govyadina from '~/assets/images/banner_govyadina.png'
    import banner_cotleta from '~/assets/images/banner_cotleta.png'
  
  const splide = ref(null);
  
  const slides = ref([
    {
      title: 'Свинина',
      description: 'Нажмите чтобы увидеть список товаров из свинины',
      image: banner_pig
    },
    {
      title: 'Говядина',
      description: 'Нажмите чтобы увидеть список товаров из говядины',
      image: banner_govyadina
    },
    {
      title: 'Курица',
      description: 'Нажмите чтобы увидеть список товаров из курицы',
      image: banner_chicken
    },
    {
      title: 'Полуфабрикаты',
      description: 'Нажмите чтобы увидеть список товаров из полуфабрикатов',
      image: banner_cotleta
    }
  ]);
  
  const options = {
    type: 'loop',
    perPage: 1,
    perMove: 1,
    gap: '20px',
    pagination: true,
    arrows: true,
    breakpoints: {
      768: {
        perPage: 1
      }
    }
  };
  </script>
  
  <style>
  .slider-container {
    max-width: 100%;
    max-height: 800px;
    margin: 0 auto;
    position: relative;
  }
  
  .slide-content {
    border-radius: 8px;
    padding: 20px;
    text-align: center;
    height: 600px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .slide-content h3, .slide-content p{
    z-index: 2;
    color: var(--color-background);
    font-size: var(--size-font-large);
  }
  
  .slide-image {
    filter: brightness(0.6);
    position: fixed;
    width: 100%;
    height: 600px;
    margin-top: 20px;
    object-fit: cover;
  }

  </style>