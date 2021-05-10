<template>
    <section class="flex flex-wrap justify-start">
        <div class="bg-yellow-500 p-20 m-1" v-for="item in items" :key="items[item]">
            {{ item }}
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            items: ['this', 'that', 'the', 'other']
        }
    }

}
</script>

<style>

</style>