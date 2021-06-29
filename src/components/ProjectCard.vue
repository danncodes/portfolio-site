<template>
<a class="flex flex-col items-center bg-gray-blue transform hover:-translate-y-2 hover:shadow-lg duration-300" href="#">
    <figure class="h-72 w-72 bg-gray-600 projectimage border shadow-sm rounded-2xl" :style="{ 'background-image': 'url(' + projectImage + ')' }"></figure>
        <div class="bg-gray-50 border p-4 shadow-md">
            <p class="font-light italic text-gray-600 text-sm">Featured Project</p>
            <h3 class="font-bold text-gray-800 text-lg mb-4 text-md" projectName>{{ projectName }}</h3>

            <p class="font-normal text-sm text-gray-500 mb-4" projectDescription>{{ projectDescription }}</p>

            <p class="font-medium text-gray-600 mb-4 text-sm" projectStack>{{projectStack }}</p>
            <div class="text-gray-800 mb-4">
                <i class="fab fa-github"></i>
                <i class="fas fa-external-link-alt ml-2"></i>
        </div>
    </div>
</a>

</template>

<script>
import Button from "./Button.vue"
export default {
    props: ["projectName","projectDescription","projectStack", "projectImage"],
    components: {Button},
    data(){
        return{
            cardHover: false,

        }
    },
    methods: {
        toggleCardSection(){
            this.cardHover = !this.cardHover
        }
    }

}
</script>
<style scoped>
figure.projectimage{
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-blend-mode: overlay;
    overflow: hidden;
    background-color: rgba(255, 255, 255, 0.1);
}

</style>
