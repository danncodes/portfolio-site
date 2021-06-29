<template>
  <a class="bg-gray-50 shadow-lg my-8 m-4 transform hover:-translate-y-2 hover:bg-gray-100 hover:shadow-xl duration-300 hover:scale-105" href="#" target="_blank">
      <figure class="relative">
        <img class="h-full w-full" alt="" :src="blogImage">
        <div class="absolute bottom-0 left-0 bg-gray-50 p-2 text-gray-700 shadow" publishDate>{{ publishDate }}</div>
      </figure>
      <div class="p-4">
          <h1 class="text-gray-700 font-bold text-lg" blogTitle>{{ blogTitle }}</h1>
          <p class="py-2" blogDescription>{{ blogDescription }}</p>
          
          <div class="flex mt-4">
              <p class="mr-2 font-light">Tags:</p>
              <p class="font-medium text-gray-700" blogTags>{{ blogTags }}</p>
          </div>
      </div>
  </a>
</template>

<script>
export default {
    props: ["publishDate", "blogTitle", "blogDescription", "blogImage", "blogTags"]

}
</script>

<style>

</style>