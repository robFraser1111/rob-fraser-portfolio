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
                    title: 'RooDigital',
                    description: 'Logo and style guide',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Homemade online',
                    description: 'Logo and style guide',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'AusIMM Bulletin',
                    description: 'Email template',
                    technologies: 'Adobe CC, Campaign Monitor and MJML',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'AusIMM video',
                    description: 'Something',
                    technologies: 'Something',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'ONCE Clothing',
                    description: 'Logo and style guide',
                    technologies: 'Adobe CC',
                    link: null,
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'SS Bricklaying',
                    description: 'Logo and style guide',
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