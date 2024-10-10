<script setup>
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
    <h1><span class="blue">{{ title }}</span></h1>
    <i>{{ msg }}</i>
</template>

<style scoped>
.blue {
  font-weight: bold;
}

h1 {
  font-size: 2.6rem;
  position: relative;
  top: -10px;
  padding: 0;
}

i {
  font-size: 0.9rem;
}

h3 {
  margin: 1rem 0;
  font-size: 1rem;
}

h1,
h3,
i {
  text-align: center;
}

@media (min-width: 1024px) {
  h1,
  h3,
  i {
    text-align: left;
  }

}
</style>
