<script setup>
</script>
<template>
    <header class="header_logo">
        <div class="desktop-header">
            <nav class="flex justify-between items-center py-5">
                <ul class="items-center gap-1  px-5 py-3  bg-[#2D3648] rounded-[6px] w-32 text-center cursor-pointer">
                    <li class="text-white">Logo</li>
                </ul>
                <ul class="flex text-[#717D96] md:gap-4 xl:gap-8 2xl:gap-12">
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center navigation cursor-pointer gap-1 "><img src="/img/Shape.svg" alt="">
                    <p>Tab</p>
                    </li>
                    <li class="flex items-center cursor-pointer px-5 py-3 gap-1 border-[#2D3648] rounded-[6px] max-w-32 border-2  hover:bg-[#2D3648] group transition-all duration-300 ease">
                        <img src="/img/icon_basket_right.svg" alt="icon_basket_right" class="group-hover:invert group-hover:brightness-0 group-hover:filter">
                        <p class="text-[#2D3648]  group-hover:text-white">Корзина</p>
                    </li>
                </ul>   
            </nav>
    </div>
    <div class="mobile-header">
            <nav class="flex justify-between items-center py-5">
                <ul class="bg-[#2D3648] rounded-[4px] text-center cursor-pointer py-3 px-10">
                    <li class="text-white">Logo</li>
                </ul>
                <ul class="flex justify-around gap-3">
                    <li class="border-[#2D3648] border-2 p-3 rounded-[4px] text-center cursor-pointer ">
                        <img src="/img/basket_icon.svg" alt="icon_basket_right"> 
                    </li>
                    <li class="border-[#2D3648] border-2 p-3 rounded-[4px] text-center cursor-pointer">
                        <img src="/img/menu.svg" alt="menu"> 
                    </li>
                </ul>  
                 
            </nav>
    </div>
</header>
  
</template>
<style scoped>
/* Скрываем мобильный хедер на десктопах */
.mobile-header {
  display: none;
}

/* Скрываем десктопный хедер на мобильных */
.desktop-header {
  display: block;
}
/* На мобильных устройствах (например, меньше 768px) */
@media (max-width: 768px) {
  .desktop-header {
    display: none;
  }
  
  .mobile-header {
    display: block;
  }
}
.header_logo{
    font-family: Inter;
    font-weight: 700;
    font-size: 16px;
}
.navigation {
    border-bottom: 2px solid transparent;
    box-sizing: border-box;
}
.navigation:hover{
    border-bottom: 2px solid #2D3648;
    transition: all 0.3s ease-in-out;
}
.navigation p {
  font-size: clamp(0.75rem, 2vw, 1rem); /* Минимум 12px, максимум 16px, адаптируется под 2% ширины экрана */
}

/* Для кнопки "Корзина" */
.basket-text {
  font-size: clamp(0.75rem, 2vw, 1rem);
}
</style>