<script setup lang="ts">
useHead(() => ({
  title: "We're going to space",
  meta: [
    {
      name: "description",
      content: "We're going to space with cruith.net",
    },
  ],
  htmlAttrs: {
    lang: "en",
  },
}));

var products = [
  { Title: "Main", Subtitle: "Home", Background: "Bg-Image", Href: "#" },
];
</script>


<template>
  <div>
    <Navbar />
    <div id="Products" class="snap-y snap-mandatory h-screen w-screen overflow-y-scroll scroll-smooth">
      <LazyProduct v-for="product in products" :key="product.Title" :Title="product.Title" :Subtitle="product.Subtitle" :Background="product.Background" :Href="product.Href" />
    </div>
  </div>
</template>


<style scoped>
::-webkit-scrollbar {
  width: 0;
}
</style>