<template>
    <div class="service-block">
        <h4 class="service-block__title">
            {{ blockTitle }}
        </h4>
        <div class="service-block__subtitle">
            <h4 class="service-block__description">
                {{ blockDescription }}
            </h4>
            <a :href="blockLink">
                <img src="../assets/link-more.svg" alt="">
            </a>
        </div>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        name: 'ServiceBlockComponent',
        props: {
            blockLink:{
                type: String,
                required: true
            },
            blockTitle: String,
            blockDescription: String

        }
    })
</script>

<style scoped lang="scss">
    .service-block {
        background-color: #8D86C9;
        padding: 20px 10px 10px;
        color: white;
        &__title {
            margin-bottom: 10px;
        }
        &__subtitle {
            display: flex;
            align-items: center;
        }
    }

</style>