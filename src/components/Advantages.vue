<template>
    <div class="advantages-block">
        <h4 class="advantages-block__title">{{ advTitle }}</h4>
        <h4 class="advantages-block__description">{{ advDescription }}</h4>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        name: 'AdvantagesComponent',
        props: {
            advTitle: String,
            advDescription: String,
        }
    })
</script>

<style scoped lang="scss">
    .advantages-block{
        background-color: rgba(192, 84, 30, 0.74);
        padding: 400px 10px 10px;
        color: white;
        &__title{
            margin-bottom: 20px;
        }
    }
    h4{
        text-align: center;
    }
</style>