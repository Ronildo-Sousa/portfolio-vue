<script setup>
  import Card from './components/Card.vue'
</script>

<template>
  <div class="bg-red-300 text-white">
    <Card 
      :title="'teste tile'"
      :description="'some description here...'"
      :link="'https://github.com/Ronildo-Sousa'"
      :link_text="'Ver detalhes'"
     />
    
  </div>
</template>