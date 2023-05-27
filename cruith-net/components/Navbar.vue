<script setup lang="ts">
const rightMenu: any = [];

const centerMenu = [
  {
    name: "Main",
    href: "#Main",
  },
];
</script>

<template>
  <div class="fixed top-0 z-20 w-screen">
    <div class="flex justify-between items-center pt-5">
      <a class="flex-1 ml-8 lg:ml-12" href="#" aria-label="Homepage">

      </a>
      <div class="grow">
        <ul class="flex-row justify-center flex font-Gotham text-sm">
          <li v-for="item in centerMenu" :key="item.name" class="mr-8 lg:block hidden select-none rounded">
            <a :href="item.href">{{ item.name }}</a>
          </li>
        </ul>
      </div>
      <div class="flex-1">
        <ul class="flex-row justify-end flex font-Gotham text-sm">
          <li v-for="item in rightMenu" :key="item.name" class="mr-8 lg:block hidden select-none">
            <a :href="item.href">{{ item.name }}</a>
          </li>
          <li class="mr-8 select-none" href="#"><a href="#">Menu</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
li {
  padding: 8px;
  border-radius: 12px;
  transition: all 0.2s ease-in-out;
  cursor: pointer;
}

a {
  color: white;
}

li:hover {
  background-color: rgba(255, 255, 255, 0.5);
}
</style>