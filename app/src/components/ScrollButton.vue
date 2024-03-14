<template>
    <button @click="scrollToSection" class="px-6 py-3 bg-blue-500 text-white font-semibold rounded-md hover:bg-blue-600 transition duration-300">
      <slot></slot>
    </button>
  </template>
  
  <script setup>
  
  const props = defineProps({
    targetId: String
  });
  
  function scrollToSection() {
    const section = document.getElementById(props.targetId);
    if (section) {
      section.scrollIntoView({ behavior: 'smooth' });
    }
  }
  </script>