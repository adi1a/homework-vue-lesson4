<template>
    <div class="container" :class="styleType">
        <template>
            <slot>

            </slot>
        </template>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        name: 'ContainerComponent',
        props: {
            styleType: String,
        }

    })
</script>

<style scoped lang="scss">
    .container{
        width: 1300px;
        margin: auto;
    }

    .container.grid{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        grid-gap: 20px;
    }
</style>