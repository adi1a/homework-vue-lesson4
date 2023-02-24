<template>
    <div class="some" :class="styleSome">
        <template>
            <slot>

            </slot>
        </template>
    </div>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        name: 'Some',
        props: {
            styleSome: String,
        }

    })
</script>

<style scoped lang="scss">
    .some{
        width: 1000px;
        margin: auto;
        padding-top: 100px;
    }

    .some.grid{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        grid-gap: 20px;
    }
</style>