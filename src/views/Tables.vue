<template>
    <div>
        <h3>Les tables de multiplications</h3>
        <input type="radio" id="10" name="10" value="10" v-model="choice">
        <label for="10">10</label>
        <input type="radio" id="13" name="13" value="13" v-model="choice">
        <label for="13">13</label><br>
        <LesTables v-bind:choice="parseInt(choice)"/>
    </div>
</template>

<script>
    import LesTables from '../components/LesTables.vue'
    export default {
        name: 'tables',
        data: function () {
            return {
                choice: 10
            }
        },
        components: {
            LesTables,
        }
    }
</script>