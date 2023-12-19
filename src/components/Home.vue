<!-- *********** HTML *********** -->
<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
  </Layout>

</template>

<!-- *********** JavaScript *********** -->
<script>
  import Header from "./Header.vue";
  import Layout from "./Layout.vue";

  export default {
    components: {
      Header,
      Layout,
    },
  };
</script>

<!-- *********** CSS *********** -->
<style>
</style>
