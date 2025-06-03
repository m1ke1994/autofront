<script></script>
<template>
 <div class="blockMenu flex flex-col">
   <ul class="flex justify-between gap-3  ">
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>По параметрам</p>
    </li>
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>По автомобилю</p>
    </li>
   </ul>
   <ul class="flex gap-2 mx-auto py-3">
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>Все</p>
    </li>
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>Премиум</p>
    </li>
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>Китай</p>
    </li>
    <li class="flex gap-1  border-[#2D3648] border-2 rounded-[4px] p-[12px]">
        <img src="/img/Shape.svg" alt="">
        <p>БУ</p>
    </li>
   </ul>
   <div class="w-full py-[8px]">
    <label for="widht" class="flex flex-col gap-2">
        <div class="flex justify-between">
             <p class="text-left widht">Ширина</p>
             <p></p>
        </div>
        <select type="text" name="" id="widht" class=" border-2 border-[#A0ABC0] bg-white w-full pl-2 p-3 rounded-[6px]">
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
        </select>
        
    </label>
   </div>
   <div class="w-full py-[8px]">
    <label for="widht" class="flex flex-col gap-1">
        <div class="flex justify-between">
             <p class="text-left widht">Диаметр</p>
             <p></p>
        </div>
        <select type="text" name="" id="widht" class=" border-2 border-[#A0ABC0] bg-white w-full pl-2 p-3 rounded-[6px]">
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
        </select>
        
    </label>
   </div>
   <div class="w-full py-[8px]">
    <label for="widht" class="flex flex-col gap-1">
        <div class="flex justify-between">
             <p class="text-left widht">Профиль</p>
             <p></p>
        </div>
        <select type="text" name="" id="widht" class=" border-2 border-[#A0ABC0] bg-white w-full pl-2 p-3 rounded-[6px]">
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
            <option value="1">Все</option>
        </select>
        
    </label>
   </div>
   <div class="w-full py-[8px]">
    <label for="widht" class="flex flex-col gap-1">
        <div class="flex justify-between">
             <p class="text-left widht">Сезон</p>
             <p></p>
        </div>
        <select type="text" name="" id="widht" class=" border-2 border-[#A0ABC0] bg-white w-full pl-2 p-3 rounded-[6px]">
            <option value="1">Любой</option>
            <option value="1">Любой</option>
            <option value="1">Любой</option>
            <option value="1">Любой</option>
            <option value="1">Любой</option>
            <option value="1">Любой</option>
            <option value="1">Любой</option>
        </select>
        
    </label>
   </div>
   <hr class="border-[#E2E7F0] my-3">
   <button class="w-full py-3 text-center text-[#2D3648] rounded-[6px]">Сбросить параметры</button>
 </div>
   
  
</template>
<style scoped>
button {
    box-sizing: border-box;
    font-size: 14px;
    font-family: "Inter", sans-serif;
    font-weight: 700;
    color: #2D3648;
    border: 2px solid #2D3648;
}
.widht{
    font-weight: 600;
    font-size: 14px;
}
p {
    font-size: 14px;
    font-family: "Inter", sans-serif;
    font-weight: 400;
    color: #2D3648;
    text-align: center;
}

.blockMenu {
    width: 350px;
    height: auto;
    border-radius: 8px;
    border-width: 1px;
    padding: 12px;
    border: 1px solid #A0ABC0;
}
</style>