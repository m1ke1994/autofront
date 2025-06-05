<script setup>
import HeaderApp from "./components/HeaderApp.vue";
import Footer from "./components/Footer.vue";
import HeaderNav from "./components/HeaderNav.vue";
import HeaderNavTwoLevel from "./components/HeaderNavTwoLevel.vue";
import Promotion from "./components/Promotion.vue";
import Reviews from "./components/Reviews.vue";
</script>
<template>
  <div class="w-full h-full">
    <div id="conteiner">
      <HeaderApp />
    </div>
    <hr class="border-2 border-[#2D3648]" />
    <div class="flex flex-col items-center gap-4">
      <HeaderNav></HeaderNav>
      <HeaderNavTwoLevel></HeaderNavTwoLevel>
      <Promotion></Promotion>
      <Reviews></Reviews>
    </div>
    <div>
      <Footer></Footer>
    </div>

    
  </div>
</template>

<style scoped>
/* Скрываем мобильный хедер на десктопах */
.mobile-title {
  display: none;
}

/* Скрываем десктопный хедер на мобильных */
.desktop-title {
  display: block;
}
/* На мобильных устройствах (например, меньше 768px) */
@media (max-width: 768px) {
  .desktop-title {
    display: none;
  }
  
  .mobile-title {
    display: block;
  }
}
p {
  font-weight: 400;
  font-size: 14px;
}
.header_logo {
  font-family: Inter;
  font-weight: 700;
  font-size: 16px;
}

footer {
  background-color: #1a202c;
  height: 229px;
  padding-top: 64px;
  padding-bottom: 64px;
}
</style>






