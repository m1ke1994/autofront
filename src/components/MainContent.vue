<script setup>
import { ref } from 'vue'
const items=[
    {
        "name": "Formula Ice Fr",
        "price": 9453,
        "total_price": 37890,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["185", "65", "R15", "H", "88"],
        "quantity":["2","4","6","8"]
    },
    {
        "name": "Winter Grip XT",
        "price": 10200,
        "total_price": 40800,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["195", "60", "R16", "T", "92"],
        "quantity":["2","4","6","8"]
    },
    {
        "name": "Arctic Speed Pro",
        "price": 11250,
        "total_price": 45000,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["205", "55", "R17", "V", "95"],
        "quantity":["2","4","6","8"]
    },
     {
        "name": "Formula Ice Fr",
        "price": 9453,
        "total_price": 37890,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["185", "65", "R15", "H", "88"],
        "quantity":["2","4","6","8"]
    },
    {
        "name": "Winter Grip XT",
        "price": 10200,
        "total_price": 40800,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["195", "60", "R16", "T", "92"],
        "quantity":["2","4","6","8"]
    },
    {
        "name": "Arctic Speed Pro",
        "price": 11250,
        "total_price": 45000,
        "image": "/img/photoImg.png",
        "alternative_image": "/img/photoImg2.png",
        "specifications": ["205", "55", "R17", "V", "95"],
        "quantity":["2","4","6","8"]
    },
]

</script>
<template>
<div class=" flex flex-col gap-4">
    <div class="flex flex-col text-left gap-4">
        <h1 class="text-3xl font-bold text-[#A0ABC0]">Диски Ши</h1>
        <h2 class="text-xl font-bold text-[#717D96]">hbuhbhbhbbhbh</h2>
    </div>
    <div class="flex items-center justify-between">
        <p>Найдено 1889 товаров</p>
        <ul >
            <li class="flex gap-1 border-[#2D3648] border-2 rounded-[4px] p-[12px]">
            <img src="/img/Shape.svg" alt="">
            <p>По популярности</p>
        </li>
        </ul>
    </div>
    <div class="xl:grid grid-cols-3 gap-10">
       <!--  <div class="card">
            <div class="flex flex-col gap-4 m-auto p-[12px] ">
            <div class="photo_image">
                <img src="/img/photoImg.png" alt="">
                <div class="photo_image2">
                    <img src="/img/photoImg2.png" alt="">
                </div>
            </div>
            <p class="title  text-left font-bold">Formula Ice Fr</p>
            <ul class="flex gap-2.5">
                <li class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px]">185</li>
                <li class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px]">65</li>
                <li class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px]">R15</li>
                <li class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px]">H</li>
                <li class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px]">88</li>
            </ul>
            </div>
            <div class="bg-[#E2E7F0] rounded-b-[6px] pb-[5px]">
                <ul class="flex items-center justify-between p-2">
                    <li class="price">9 453 <span>Р</span></li>
                    <li><img src="/img/Vector.svg" alt="line"></li>
                    <li class="generalPrice">37 890 <span>Р</span> за 4 шт.</li>
                </ul>
                <ul class="flex items-center justify-around">
                    <li class="generalPrice border-2 border-[#2D3648] py-1 px-3 rounded-[4px] text-center">2 <span>шт</span></li>
                    <li class="generalPrice border-2 border-[#2D3648] py-1 px-3 rounded-[4px] text-center">4 <span>шт</span></li>
                    <li class="generalPrice border-2 border-[#2D3648] py-1 px-3 rounded-[4px] text-center">6 <span>шт</span></li>
                    <li class="generalPrice border-2 border-[#2D3648] py-1 px-3 rounded-[4px] text-center">8 <span>шт</span></li>
                </ul>
                <div class="flex flex-col gap-2 justify-center items-center p-2 ">
                    <button class="border-2 border-[#2D3648] text-center px-[12px] py-[10px] w-full rounded-[6px] text-[#2D3648] font-bold">Добавить в корзину</button>
                    <button class="border-2 border-[#2D3648] text-center px-[12px] py-[10px] w-full rounded-[6px] text-[#2D3648] font-bold">Быстрый заказ</button>
                </div>
            </div>
            </div> -->
        <div v-for="(item, index) in items" :key="index" class="card">
      <div class="flex flex-col gap-4 m-auto p-[12px] mb-2">
        <div class="photo_image w-full">
          <img :src="item.image" alt="" >
          <div class="photo_image2">
            <img :src="item.alternative_image" alt="">
          </div>
        </div>
        <p class="title text-left font-bold">{{ item.name }}</p>
        <ul class="flex gap-2.5">
          <li v-for="spec in item.specifications" :key="spec" class="p-1 w-10 text-center bg-[#CBD2E0] rounded-[4px] pb-2">
            {{ spec }}
          </li>
        </ul>
      </div>
      <div class="bg-[#E2E7F0] rounded-b-[6px] pb-[5px] pt-2">
        <ul class="flex items-center justify-between p-2">
          <li class="price">{{ item.price }} <span>Р</span></li>
          <li><img src="/img/Vector.svg" alt="line"></li>
          <li class="generalPrice">{{ item.total_price }} <span>Р</span> за 4 шт.</li>
        </ul>
        <ul class="flex items-center justify-around">
          <li v-for="qty in item.quantity" :key="qty" class="generalPrice border-2 border-[#2D3648] py-1 px-3 rounded-[4px] text-center">
            {{ qty }} <span>шт</span>
          </li>
        </ul>
        <div class="flex flex-col gap-2 justify-center items-center p-2">
          <button class="border-2 border-[#2D3648] text-center px-[12px] py-[10px] w-full rounded-[6px] text-[#2D3648] font-bold">
            Добавить в корзину
          </button>
          <button class="border-2 border-[#2D3648] text-center px-[12px] py-[10px] w-full rounded-[6px] text-[#2D3648] font-bold">
            Быстрый заказ
          </button>
        </div>
      </div>
    </div>    
            
  
            
           <div>

           </div> 
        
    </div>
    
</div>
</template>
<style scoped>
.photo_image img,.photo_image2 img {
  width: 100%; /* Заполняет всю ширину родительского контейнера */
  height: auto; /* Сохраняет пропорции изображения */
  object-fit: cover; /* Гарантирует адекватное заполнение контейнера */
}


.generalPrice{

}
.price{
    font-weight: 700;
    font-size: 16px;  
}
.generalPrice{
    font-weight: 400;
    font-size: 12px;
    line-height: 15px;
    color: #2D3648;
}
.title{
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
    color: #2D3648;
}

.card{
width: auto;
height: auto;
border-radius: 16px;
border-width: 1px;
}
.photo_image{
    position: relative;
    margin: auto;
}
.photo_image2{
    position: absolute;
    top: 16px;
    left: 16px;
}
</style>