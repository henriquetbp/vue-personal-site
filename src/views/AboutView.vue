<script setup>
import Title from '../components/utils/Title.vue'
</script>

<template>
  <div class="about">
      <img alt="Imagem de perfil" class="profile-img" src="@/assets/img/profile-image.png" width="70%" />
    <div>
    <Title title="Sobre" msg='"A imaginação é mais importante que o conhecimento, porque o conhecimento é limitado, ao passo que a imaginação abrange o mundo inteiro" - Albert Einstein' />
  </div>
    <p>Sou desenvolvedor web desde 2016, com experiência em projetos personalizados. Apaixonado por criar soluções web eficientes e inovadoras, utilizando as mais recentes tecnologias. Trabalho de forma flexivel, garantindo perfomance e agilidade.</p>
    <p>Saiba mais em <a href="http://torquato.dev" target="_blank" rel="noopener noreferrer">torquato.dev</a></p>
  </div>
</template>

<style>
.about {
  text-align: center;
}

.about img {
  max-width: 70%;
  margin: 2rem 0;
}

.about p {
  margin: 1rem 0;
  width: 100%;
}

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: start;
  }

  .about img {
    margin: 0 0 2rem 0;
  }
}
</style>
