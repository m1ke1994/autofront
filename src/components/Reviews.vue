<template>
    <hr class="border-1 border-[#A0ABC0] w-full">
  <div id="conteiner">
    <section id="promotion" class="w-full h-auto rounded-[6px] border-2 border-[#A0ABC0] p-[16px] my-[16px]">
      <h1 class="text-xl text-black font-bold mb-4">Отзывы</h1>
      
      <!-- Mobile slider -->
      <div 
        class="mobile-slider-container relative block md:hidden overflow-hidden"
        @mouseenter="pauseAutoSlide"
        @mouseleave="resumeAutoSlide"
      >
        <div 
          class="mobile-slider-track flex transition-transform duration-300 ease-in-out"
          :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
        >
          <div v-for="(slide, index) in slides" :key="index" class="mobile-slide min-w-full">
            <img :src="slide.image" alt="" class="w-full">
          </div>
        </div>
        
        <!-- Navigation dots -->
        <div class="flex justify-center mt-4">
          <span 
            v-for="(dot, index) in slides" 
            :key="index"
            class="dot w-3 h-3 mx-1 rounded-full bg-gray-300 cursor-pointer"
            :class="{ 'active': index === currentIndex }"
            @click="goToSlide(index)"
          ></span>
        </div>
        
        <!-- Navigation arrows -->
        <button 
          class="slider-arrow absolute left-2 top-1/2 transform -translate-y-1/2 bg-white bg-opacity-70 rounded-full w-8 h-8 flex items-center justify-center shadow-md"
          @click="prevSlide"
        >
          &larr;
        </button>
        <button 
          class="slider-arrow absolute right-2 top-1/2 transform -translate-y-1/2 bg-white bg-opacity-70 rounded-full w-8 h-8 flex items-center justify-center shadow-md"
          @click="nextSlide"
        >
          &rarr;
        </button>
      </div>
      <button class=" border-2 border-[#2D3648] text-bg-[#2D3648] rounded-[4px] p-[10px] mt-[24px] w-full hover:text-white hover:bg-[#2D3648] transition-colors duration-300">Смотреть все</button>
      
      <!-- Desktop grid -->
      
    </section>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const slides = ref([
  { image: '/img/image.png' },
  { image: '/img/image.png' },
  { image: '/img/image.png' }
]);

const currentIndex = ref(0);
let slideInterval = null;
let touchStartX = 0;
let touchEndX = 0;

const updateSlider = () => {
  // В Vue реактивность сама обновит представление
};

const goToSlide = (index) => {
  currentIndex.value = index;
};

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % slides.value.length;
};

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + slides.value.length) % slides.value.length;
};

const startAutoSlide = () => {
  slideInterval = setInterval(nextSlide, 3000);
};

const pauseAutoSlide = () => {
  clearInterval(slideInterval);
};

const resumeAutoSlide = () => {
  pauseAutoSlide();
  startAutoSlide();
};

const handleTouchStart = (e) => {
  touchStartX = e.changedTouches[0].screenX;
};

const handleTouchEnd = (e) => {
  touchEndX = e.changedTouches[0].screenX;
  handleSwipe();
};

const handleSwipe = () => {
  const threshold = 50;
  
  if (touchEndX < touchStartX - threshold) {
    nextSlide();
  } else if (touchEndX > touchStartX + threshold) {
    prevSlide();
  }
};

onMounted(() => {
  const sliderContainer = document.querySelector('.mobile-slider-container');
  if (sliderContainer) {
    sliderContainer.addEventListener('touchstart', handleTouchStart, { passive: true });
    sliderContainer.addEventListener('touchend', handleTouchEnd, { passive: true });
  }
  startAutoSlide();
});

onBeforeUnmount(() => {
  const sliderContainer = document.querySelector('.mobile-slider-container');
  if (sliderContainer) {
    sliderContainer.removeEventListener('touchstart', handleTouchStart);
    sliderContainer.removeEventListener('touchend', handleTouchEnd);
  }
  pauseAutoSlide();
});
</script>

<style scoped>
.mobile-slider-container {
  touch-action: pan-y;
}

.mobile-slider-track {
  will-change: transform;
}

.dot.active {
  background-color: #4A5568;
}

.slider-arrow {
  z-index: 10;
}
</style>