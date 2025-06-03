<script></script>
<template>
    <div class="header_logo">
        <div>
            <nav class="flex justify-between items-center py-5">
                <ul class="items-center gap-1  px-5 py-3  bg-[#2D3648] rounded-[6px] w-32 text-center cursor-pointer">
                    <li class="text-white">Logo</li>
                </ul>
                <ul class="flex text-[#717D96] gap-8">
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
                    <li class="flex items-center cursor-pointer px-5 py-3 gap-1 border-[#2D3648] rounded-[6px] max-w-32 border-2"><img src="/img/icon_basket_right.svg" alt="icon_basket_right">
                    <p class="text-[#2D3648]">Корзина</p>
                    </li>
                </ul>   
            </nav>
    </div>
</div>
  
</template>
<style scoped>
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
</style>