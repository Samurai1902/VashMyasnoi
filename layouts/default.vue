<template>
  <div class="page">
    <header class="header">
      <div class="container">
        <NuxtLink to="/" class="logo">Ваш мясной</NuxtLink>
        <nav class="nav">
          <ul class="nav-list">
            <li class="nav-item" v-for="(link, index) in links" :key="index">
              <NuxtLink :to="link.url" class="nav-link">{{ link.text }}</NuxtLink>
            </li>
          </ul>
        </nav>
        <!-- <a href="tel:89201425003" class="phone">+7 (920) 142-50-03</a> -->
      </div>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer class="footer">
      <div class="container">
        <p>© 2023 Ваш мясной. Все права защищены.</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
const links = [
  { text: 'Главная', url: '/' },
  { text: 'Каталог', url: '/catalog' },
  { text: 'О нас', url: '/about' },
  { text: 'Контакты', url: '/contacts' },
]
</script>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  background-color: transparent;
  color: var(--color-white);
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.logo {
  font-size: var(--size-font-large);
  font-weight: bold;
  color: var(--color-white);
  text-decoration: none;
}

.nav-list {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-item {
  margin: 0 15px;
}

.nav-link {
  position: relative;
  text-decoration: none;
  color: var(--color-white);
  font-size: var(--size-font-small);
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: var(--color-secondary);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: var(--color-secondary);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.3s ease;
}

.nav-link:hover::after {
  transform: scaleX(1);
}

.nav-link:not(:hover)::after {
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.3s ease;
}

.phone {
  font-size: var(--size-font-small);
  font-weight: bold;
  text-decoration: none;
  color: var(--color-white);
}

.footer {
  background-color: var(--color-primary);
  color: var(--color-white);
  padding: 20px 40px;
  text-align: center;
  border-radius: 15px 15px 0px 0px;
}
</style>