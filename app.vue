<template>
  <div class="flex justify-center items-center h-screen bg-gray-700">
    <div class="relative w-52 h-52 rounded-full">
      <div class="text w-full h-full text-center">
        <p>
          <span
            v-for="(char, index) in text"
            :key="index"
            :style="{ transform: `rotate(${index * 6.5}deg) translate(-50%, -50%)` }"
            class="absolute"
          >{{ char }}</span>
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';

  const text = ref('Qreative - Web Agency - Nivelles - Digitale Strategy -');
</script>

<style scoped>
  .text {
    animation: rotateText 10s linear infinite;
    color: rgb(79, 227, 79);
  }

  .text span {
    font-size: 1.2em;
    transform-origin: 0 100px;
  }

  @keyframes rotateText {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>