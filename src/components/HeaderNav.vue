<script>
</script>
<template>
    <div id="conteiner">
      <section class="desktop-title w-8/12 mx-auto mt-8 mb-8 ">
        <div class="bg-[#717D96] w-full h-16"></div>
      </section>
       <section class="mobile-title mx-auto mt-6 mb-6 flex flex-col gap-2">
        <div class="bg-[#717D96] w-[full] h-10"></div>
        <div class=" w-[full] h-6"></div>
        <div class="bg-[#717D96] w-[80%] mx-auto h-10"></div>
      </section>
      <section class="flex flex-col gap-2 md:flex-row md:w-8/12 md:justify-center md:mx-auto md:items-center">
        <ul class="flex justify-between md:w-[50%]">
           <li class="flex justify-center  gap-3 items-center border-2 border-[#2D3648] rounded-lg p-2 w-[49%] cursor-pointer hover:bg-[#2D3648] group transition-colors duration-300 md:flex-col  md:min-w-[110px] md:min-h-[110px]">
            <img
              src="/img/Shape.svg"
              alt="Shape"
              class="group-hover:brightness-0 group-hover:invert"
            />
            <p class="group-hover:text-white">Шины</p>
          </li>
            <li class="flex justify-center gap-3 items-center border-2 border-[#2D3648] rounded-lg p-2 w-[49%] cursor-pointer hover:bg-[#2D3648] group transition-colors duration-300 md:flex-col  md:min-w-[110px] md:min-h-[110px]">
            <img
              src="/img/Shape.svg"
              alt="Shape"
              class="group-hover:brightness-0 group-hover:invert"
            />
            <p class="group-hover:text-white">Диски</p>
          </li>
        </ul>
        <ul class="max-md:hidden">
          <li>
            <img class="transform rotate-90" src="/img/Vector.svg" alt="Vector" />
          </li>
        </ul>
          <ul class="flex justify-between items-center md:w-[50%]">
           <li class="flex justify-center  gap-3 items-center border-2 border-[#2D3648] rounded-lg p-2 w-[49%] cursor-pointer hover:bg-[#2D3648] group transition-colors duration-300 md:flex-col  md:min-w-[110px] md:min-h-[110px] text-center">
            <img
              src="/img/Shape.svg"
              alt="Shape"
              class="group-hover:brightness-0 group-hover:invert"
            />
            <p class="group-hover:text-white">По параметрам</p>
          </li>
            <li class="flex justify-center gap-3 items-center border-2 border-[#2D3648] rounded-lg p-2 w-[49%] cursor-pointer hover:bg-[#2D3648] group transition-colors duration-300 md:flex-col  md:min-w-[110px] md:min-h-[110px] text-center">
            <img
              src="/img/Shape.svg"
              alt="Shape"
              class="group-hover:brightness-0 group-hover:invert"
            />
            <p class="group-hover:text-white">По автомобилю</p>
          </li>
        </ul>
      </section>
     
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
