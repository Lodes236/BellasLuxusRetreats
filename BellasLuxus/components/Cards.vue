<template>
    <div :style="{ backgroundColor: background}">
        <div class="box element-cards t-center">
            <div class="element-cards-text" :style="{ color: textColor }">
                <h2>{{ headline }}</h2>
                <p>{{ text }}</p>
            </div>
            <div class="element-cards-boxes flex justify-around">
                <div class="element-cards-boxes-img w-40" style="background-image: url('https://picsum.photos/500/300');"></div>

                <div :style="{ backgroundColor: backgroundTwo}" class="w-40 flex justify-center align-center">
                    <p>
                        {{ boxText }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  // Define the props that the component will accept
  const props = defineProps({
    background: {
      type: String,
      required: true,
      default: 'rgb(255, 254, 246)', // default white color
    },
    backgroundTwo: {
        type: String,
        required: true,
        default: '#ffffff',
    },
    headline: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
      default: 'white',
    },
    textColor: {
      type: String,
      required: true,
    },
    boxText: {
        type: String,
        required: true,
    }
  });
  </script>
  
  <style scoped>

  </style>
