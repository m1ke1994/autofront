<script></script>
<template>
  <footer>
    <div class="flex flex-col justify-between gap-8" id="conteiner">
      <div class="flex flex-col gap-8 text-white">
        <p
          class="header_logo px-5 py-3 bg-[#2D3648] rounded-[6px] w-32 text-center cursor-pointer h-full"
        >
          Logo
        </p>
      </div>
      <div class="flex justify-between max-md:flex-col  gap-4">
        <div >
          <p class="text-white">Copyright 2022 Company Name.</p>
        </div>
        <div class="flex gap-4 max-md:flex-col">
          <p
            class="text-white opacity-50 hover:opacity-100 transition-opacity duration-300 cursor-pointer"
          >
            Privacy Policy
          </p>
          <p
            class="text-white opacity-50 hover:opacity-100 transition-opacity duration-300 cursor-pointer"
          >
            Terms & Conditions
          </p>
          <p
            class="text-white opacity-50 hover:opacity-100 transition-opacity duration-300 cursor-pointer"
          >
            Cookie Policy
          </p>
          <p
            class="text-white opacity-50 hover:opacity-100 transition-opacity duration-300 cursor-pointer"
          >
            Contact
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>
<style scoped>
@media (max-width: 768px) {
    p {
        font-weight: 400;
        font-size: 12px;
    }
}
.header_logo{
    font-family: Inter;
    font-weight: 700;
    font-size: 16px;
}

footer {
    background-color: #1A202C;
   
    max-width: 100%;
    overflow: hidden;
}

</style>
