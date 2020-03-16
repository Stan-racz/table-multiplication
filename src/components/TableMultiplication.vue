<template>
  <div>
    <h3>Table de {{n}}</h3>
    <table class="table-multiplication" >
      <tbody>
        <TableRow v-for="nombre in 9" v-bind:j="nombre" v-bind:i="n"/>
      </tbody>
    </table>
    <br/>
  </div>
</template>

<script>
  import TableRow from "./TableRow.vue";
  export default {
    name: "TableMultiplication",
    components: {
      TableRow
    },
    props: {
      n: Number
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .table-multiplication {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    background-color: lightblue;
  }
</style>
