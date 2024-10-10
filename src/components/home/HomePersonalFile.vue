k<script setup>
import HomeItem from './HomeItem.vue'
import Divisor from '../utils/Divisor.vue'
import BookIcon from '../icons/IconBook.vue'
import DesktopIcon from '../icons/IconDesktop.vue'
import EcosystemIcon from '../icons/IconEcosystem.vue'
import PersonalCheckIcon from '../icons/IconPersonalCheck.vue'
import HeartIcon from '../icons/IconHeart.vue'
</script>

<template>
  <HomeItem>
    <template #icon>
      <BookIcon />
    </template>
    <template #heading>Formação</template>
      <p>Curso Superior de Tecnologia em Radiologia - UFMG <span class="blue">(Concluído)</span></p>
      <p>Sistema para Internet - UNOPAR <span class="blue">(Cursando)</span></p>
  </HomeItem>

  <HomeItem>
    <template #icon>
      <DesktopIcon />
    </template>
    <template #heading>Área de Atuação</template>
    <p><span class="blue">Desenvolvedor Web Full Stack</span></p>
    <p>Desenvolvimento de soluções web personalizadas para  automação e otimização de processos, e manipulação de dados.</p>

  </HomeItem>

  <HomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Tecnologias</template>
    <p><span class="blue">Laravel</span> - Backend</p>
    <p><span class="blue">Vue.js</span> - FrontEnd</p>
    <p><span class="blue">MySQL</span> - Banco de Dados</p>
  </HomeItem>

  <HomeItem>
    <template #icon>
      <PersonalCheckIcon />
    </template>
    <template #heading>Experiências</template>
    <p>Densenvolvimento de API's REST</p>
    <p>Densenvolvimento de Sistemas Web</p>
    <p>Densenvolvimento de Sites</p>
    <p>Densenvolvimento de E-commerces</p>
  </HomeItem>

  <HomeItem>
    <template #icon>
      <HeartIcon />
    </template>
    <template #heading>Habilidades Pessoais</template>
    <p>Proativo <Divisor/> Comunicativo <Divisor/> Dedicado</p>
  </HomeItem>
</template>