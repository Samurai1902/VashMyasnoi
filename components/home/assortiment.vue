<template>
    <section class="assortment">
        <h2>Наш ассортимент</h2>
        <p>
            Мы предлагаем широкий выбор свежего мяса: свинина, курица, говядина и многое другое.
            Все продукты высшего качества, от проверенных поставщиков.
        </p>
        <div class="assortment-icons">
            <div class="assortment-icon">
                <p>Свинина</p>
                <img src="~/assets/images/pig.png" alt="Свинина">
            </div>
            <div class="assortment-icon">
                <p>Говядина</p>
                <img src="~/assets/images/govyadina.png" alt="Говядина">
            </div>
            <div class="assortment-icon">
                <p>Бараннина</p>
                <img src="~/assets/images/sheep.png" alt="Бараннина">
            </div>
            <div class="assortment-icon">
                <p>Индейка</p>
                <img src="~/assets/images/turkey.png" alt="Индейка">
            </div>
            <div class="assortment-icon">
                <p>Курица</p>
                <img src="~/assets/images/chicken.png" alt="Курица">
            </div>
            <div class="assortment-icon">
                <p>Полуфабрикаты</p>
                <img src="~/assets/images/cotleta.png" alt="Полуфабрикаты">
            </div>
            <div class="assortment-icon">
                <p>Маринады и приправы</p>
                <img src="~/assets/images/marinade.png" alt="Маринады">
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style >
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
        padding: 60px 20px;
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