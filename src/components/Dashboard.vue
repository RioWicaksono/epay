<template>
  <div class="w-full bg-gradient-to-r from-blue-400 to-black text-white flex flex-col relative w-full overflow-x-hidden">
    Header with Navbar
    <header 
      :class="['fixed top-0 left-0 w-full px-6 py-3 flex justify-between items-center z-50 transition-transform duration-300', showHeader ? 'translate-y-0' : '-translate-y-full']">
      <h1 
        class="text-4xl font-extrabold cursor-pointer bg-gradient-to-r from-blue-200 via-white to-red-400 bg-clip-text text-transparent tracking-widest"
        @mouseover="hoverEffect = true"
        @mouseleave="hoverEffect = false"
        :style="hoverEffect ? { transform: 'scale(1.2) rotate(5deg)', color: '#ffcc00' } : {}">
        E-Pay
      </h1>
      <div class="flex gap-6">
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-5 rounded-lg text-sm shadow-lg transition-transform transform hover:scale-105">Sign Up</button>
        <button class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-5 rounded-lg text-sm shadow-lg transition-transform transform hover:scale-105">Login</button>
      </div>
    </header>
    
    <div class="flex-1 flex flex-col items-center justify-center mt-20 px-4 w-full">
      <!-- Dynamic Image Section with Slogan -->
      <div class="flex flex-col items-center mt-6 w-full max-w-2xl">
        <img 
          src="https://seeklogo.com/images/E/electronic-payments-logo-4417B90598-seeklogo.com.png" 
          alt="E-Payment Illustration" 
          class="w-full max-w-xs h-auto drop-shadow-lg"
        />
        <h2 
          class="mt-4 text-3xl font-bold text-center bg-gradient-to-r from-yellow-300 to-red-500 bg-clip-text text-transparent tracking-widest uppercase cursor-default">
          "Seamless Transactions, Limitless Possibilities!"
        </h2>
      </div>
      
      <!-- Services Section -->
      <div class="mt-10 text-center w-full px-6 max-w-5xl">
        <h3 class="text-3xl font-bold text-blue-300 cursor-default animate-bounce">Our Services</h3>
        <div class="mt-4 grid grid-cols-1 sm:grid-cols-3 gap-6">
          <div class="bg-gray-800 p-4 rounded-lg shadow-lg cursor-pointer hover:scale-105 transition-transform">
            <h4 class="text-xl font-semibold text-red-400">Fast Transactions</h4>
            <p class="text-gray-300 mt-2">Experience real-time payment processing with security.</p>
          </div>
          <div class="bg-gray-800 p-4 rounded-lg shadow-lg cursor-pointer hover:scale-105 transition-transform">
            <h4 class="text-xl font-semibold text-yellow-400">Secure Payments</h4>
            <p class="text-gray-300 mt-2">Top-tier encryption to protect your transactions.</p>
          </div>
          <div class="bg-gray-800 p-4 rounded-lg shadow-lg cursor-pointer hover:scale-105 transition-transform">
            <h4 class="text-xl font-semibold text-blue-400">Global Reach</h4>
            <p class="text-gray-300 mt-2">Send and receive money worldwide effortlessly.</p>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Footer -->
    <footer class="p-4 text-center text-sm text-gray-300 mt-10">
      Created by R Development © 2025
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const showHeader = ref(true);
const hoverEffect = ref(false);
let lastScrollY = window.scrollY;

const handleScroll = () => {
  if (window.scrollY > lastScrollY) {
    showHeader.value = false;
  } else {
    showHeader.value = true;
  }
  lastScrollY = window.scrollY;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.animate-bounce {
  animation: bounce 2s infinite alternate;
}
@keyframes bounce {
  0% { transform: translateY(0); }
  100% { transform: translateY(-10px); }
}
</style>
