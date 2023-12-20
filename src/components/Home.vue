<!-- *********** HTML *********** -->
<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume 
        :total-label="'Total savings'"
        :label="label"
        :total-amount="totalAmount"
        :amount="amount"
      />
    </template>
    <template #movements>
      <Movements />
    </template>
  </Layout>

</template>

<!-- *********** JavaScript *********** -->
<script>
  import Header from "./Header.vue";
  import Layout from "./Layout.vue";
  import Movements from "./Movements.vue";
  import Resume from "./Resume/Index.vue";

  export default {
    components: {
      Header,
      Movements,
      Layout,
      Resume
    },
    data() {
      return {
        label: "Savings",
        totalAmount: 0,
        amount: null,
      }
    }
  };
</script>

<!-- *********** CSS *********** -->
<style>
</style>
