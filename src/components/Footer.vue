<template>
  <footer class="w-full">
    <div class="container mx-auto px-4 py-8">
      <div class="flex flex-col justify-between gap-8">
        <div class="flex flex-col gap-8 text-white">
          <p class="header_logo px-5 py-3 bg-[#2D3648] rounded-[6px] w-32 text-center cursor-pointer">
            Logo
          </p>
        </div>
        <div class="flex justify-between flex-wrap gap-4">
          <div>
            <p class="text-white text-sm md:text-base">Copyright 2022 Company Name.</p>
          </div>
          <div class="flex gap-4 flex-wrap">
            <p class="footer-link">
              Privacy Policy
            </p>
            <p class="footer-link">
              Terms & Conditions
            </p>
            <p class="footer-link">
              Cookie Policy
            </p>
            <p class="footer-link">
              Contact
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter'
}
</script>

<style scoped>
.footer-link {
  @apply text-white opacity-50 hover:opacity-100 transition-opacity duration-300 cursor-pointer text-sm md:text-base;
}

.header_logo {
  font-family: Inter;
  font-weight: 700;
  font-size: 16px;
  line-height: 1.5;
}

footer {
  background-color: #1A202C;
  width: 100%;
}

@media (max-width: 768px) {
  .container {
    padding-left: 1rem;
    padding-right: 1rem;
  }
  
  .footer-link, .header_logo {
    font-size: 12px;
  }
}
</style>