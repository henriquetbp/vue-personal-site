<script setup>
import Title from "../utils/Title.vue"

defineProps({
  title: {
    type: String,
    required: true
  },
  msg: {
    type: String,
    required: true
  }
  
})
</script>

<template>
  <div class="greetings">
    <Title title="Henrique Torquato" msg='"A única maneira de fazer um grande trabalho é amar o que você faz. - Steve Jobs"' />
    <h3>
      Conheça mais sobre o meu trabalho
    </h3>
  </div>
</template>

<style scoped>
h3 {
  margin: 1rem 0;
  font-size: 1rem;
}
</style>
