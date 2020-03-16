<template>
    <div>
        <span v-for="n in choice" :key="n">
      <p>
        <table-multiplication v-bind:n="parseInt(n)"/>&nbsp;
      </p>
    </span>
    </div>
</template>

<script>
    import TableMultiplication from './TableMultiplication.vue'
    export default {
        name: 'LesTables',
        components: {
            TableMultiplication
        },
        props: {
            n: Number,
            choice: Number
        }
    }
</script>

<style>
    p {
        display: inline-block;
        margin: 0px 20px;
    }
</style>