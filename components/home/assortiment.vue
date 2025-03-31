<template>
    <section class="assortment">
        <h2>Наш ассортимент</h2>
        <p>
            Мы предлагаем широкий выбор свежего мяса: свинина, курица, говядина и многое другое.
            Все продукты высшего качества, от проверенных поставщиков.
        </p>
        <div class="assortment-icons">
            <div 
                class="assortment-icon" 
                v-for="(item, index) in assortmentItems" 
                :key="index"
            >
                <p>{{ item.name }}</p>
                <img :src="item.image" :alt="item.name">
            </div>
        </div>
    </section>
</template>

<script setup>
import pigImg from '~/assets/images/pig.png'
import govyadinaImg from '~/assets/images/govyadina.png'
import sheepImg from '~/assets/images/sheep.png'
import turkeyImg from '~/assets/images/turkey.png'
import chickenImg from '~/assets/images/chicken.png'
import cotletaImg from '~/assets/images/cotleta.png'
import marinadeImg from '~/assets/images/marinade.png'

const assortmentItems = [
    { name: 'Свинина', image: pigImg },
    { name: 'Говядина', image: govyadinaImg },
    { name: 'Бараннина', image: sheepImg },
    { name: 'Индейка', image: turkeyImg },
    { name: 'Курица', image: chickenImg },
    { name: 'Полуфабрикаты', image: cotletaImg },
    { name: 'Маринады и приправы', image: marinadeImg },
]
</script>

<style>
    .assortment-icons{
        display: flex;
        flex-direction: row;
        gap: 100px;
        justify-content: center
    }

    .assortment-icon img{
        width: 100px;
        height: 100px;
    }

    .assortment {
        display: flex;
        flex-direction: column;
        width: 100%;
        background-color: var(--color-background);
        text-align: center;
        z-index: 1;
        gap: 30px;
        padding: 60px 0px;
    }

    .assortment h2 {
        font-size: var(--size-font-large);
        margin: 0;
    }

    .assortment p {
        font-size: var(--size-font-small);
        max-width: 800px;
        margin: 0 auto;
    }
</style>