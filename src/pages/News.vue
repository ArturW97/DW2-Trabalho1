<template>
    <div>
      <Header />
      <main>
        <NewsComponent :isButton="false" />
      </main>
  </div>
</template>
<script>
import Header from "../components/Header.vue";
import NewsComponent from "../components/NewsComponent.vue";
export default {
  name: "News",
  components: {
    Header,
    NewsComponent,
  },
};
</script>
<style></style>
