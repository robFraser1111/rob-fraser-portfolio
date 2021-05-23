<template>
    <section class="flex flex-wrap justify-center">
        <CardLong v-for="item in items" :key="items[item]" 
            :link="item.link" 
            :title="item.title"
            :description="item.description"
            :technologies="item.technologies"
            :image="item.image" 
        />
    </section>
</template>


<script>
export default {
    data() {
        return {
            items: [
                {
                    title: 'ONCE Clothing',
                    description: 'Lifestyle brand',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Business cards',
                    description: 'RooDigital and Once business cards',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Banners',
                    description: 'Football field boundary banners',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Decals',
                    description: 'Car window decals',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                }
            ]
        }
    }

}
</script>

<style>

</style>