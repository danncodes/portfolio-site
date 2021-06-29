<template>
<button btnText class="px-6 py-2 border-2 border-gray-700 outline-none bg-transparent tracking-widest rounded text-gray-700 transform hover:text-gray-000 hover:-translate-y-2 transition-all ease-in-out duration-300 shadow-md hover:shadow-2xl whitespace-nowrap">{{ btnText }}</button>
</template>

<script>
export default {
    props: [ 'btnText' ]

}
</script>

<style scoped>

</style>
