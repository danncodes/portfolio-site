<template>
<button btnText class="px-6 py-2 bg-gray-600 border-2 border-gray-600 outline-none tracking-widest rounded text-gray-200 transform hover:bg-gray-700 hover:border-gray-700 hover:text-gray-300 hover:-translate-y-2 transition-all ease-in-out duration-300 shadow-md hover:shadow-2xl whitespace-nowrap">{{ btnText }}</button>
</template>

<script>
export default {
    props: [ 'btnText' ]

}
</script>

<style scoped>

</style>
