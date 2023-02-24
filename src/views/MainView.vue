<template>
  <div class="home">
    <header class="home-header">
      <ContainerComponent :styleType="containerType.GRID">
        <ServiceBlockComponent v-for="(service, index) in services" 
          :block-link="service.link" 
          :block-title="service.title" 
          :block-description="service.description" 
          :key="index"/>
      </ContainerComponent>
    </header>

    <SomeComponent :styleSome="containerType.GRID">
      <AdvantagesComponent v-for="(advantage, index) in advantages" 
      :adv-title="advantage.title"  
      :adv-description="advantage.description" 
      :key="index"/>
    </SomeComponent>
    
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import ContainerComponent from '../components/Container.vue';
import ServiceBlockComponent from '../components/ServiceBlock.vue';
import { ContainerType } from '../constants/ContainerType';
import AdvantagesComponent from '../components/Advantages.vue';
import SomeComponent from '../components/Some.vue';

export default Vue.extend({
  name: 'HomeView',
  data: () => ({
    containerType: ContainerType, 
    services: [
      {
        title: 'Услуги',
        description: 'Аренда корта',
        link: '/'
      },
      {
        title: 'Услуги',
        description: 'Детский теннис',
        link: '/'
      },
      {
        title: 'Услуги',
        description: 'Сборы команд',
        link: '/'
      },
      {
        title: 'Турниры',
        description: 'Расписание',
        link: '/'
      }
    ],
    advantages: [
      {
        title: '5 летних',
        description: 'грунтовых кортов'
      },
      {
        title: 'Зал с покрытием',
        description: '"Искусственная трава"'
      },
      {
        title: 'Зал с покрытием',
        description: '"Хард"',
      },
    ]
  }),
  components: {
    ContainerComponent,
    ServiceBlockComponent,
    AdvantagesComponent,
    SomeComponent,
  },
});
</script>


<style scoped lang="scss" >


  .home-header{
    background-image: url('../assets/header-bg.jpg');
    padding-top: 700px;
  }
</style>
