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
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import ContainerComponent from '../components/Container.vue';
import ServiceBlockComponent from '../components/ServiceBlock.vue';
import { ContainerType } from '../constants/ContainerType';

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
    ]
  }),
  components: {
    ContainerComponent,
    ServiceBlockComponent,
  },
});
</script>


<style scoped lang="scss" >


  .home-header{
    background-image: url('../assets/header-bg.jpg');
    padding-top: 600px;
  }
</style>
