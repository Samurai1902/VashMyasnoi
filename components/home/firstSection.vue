<template>
    <section class="firstblock">
      <div class="firstblock-content">
        <img src="~/assets/images/myaso-banner.jpg" alt="Фон" class="firstblock-background" />
        <h1>Добро пожаловать в мясной магазин "Ваш мясной"</h1>
        <p>Свежее мясо каждый день!</p>
      </div>
    </section>
  </template>
  
  <script setup>
  </script>
  
  <style >
  .firstblock {
  position: relative;
  height: 600px;
  width: 100%;
  overflow: hidden;
}

.firstblock-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 800px;
  z-index: -2;
  filter: brightness(0.7);
}

.firstblock-content {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 600px;
  text-align: center;
  color: white;
  padding: 20px;
}

.firstblock h1 {
  font-size: 3rem;
  margin: 0;
}

.firstblock p {
  font-size: 1.5rem;
  margin: 10px 0 0;
}
  </style>