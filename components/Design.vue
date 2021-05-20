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
                    description: 'Digital agency',
                    technologies: 'Custom theme WordPress multisite',
                    link: 'roo.digital',
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Miiesha',
                    description: 'ARIA award winning R&B artist',
                    technologies: 'Vue website',
                    link: 'miiesha.com',
                    image: 'hello.jpg'
                },
                {
                    title: 'Joseph Vea',
                    description: 'New Zealand born, Tongan singer/songwriter',
                    technologies: 'React website',
                    link: 'josephvea.com',
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'SS Bricklaying',
                    description: 'Local bricklaying company',
                    technologies: 'WordPress website',
                    link: 'ssbricklaying.melbourne/',
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'Brick Restorations Melbourne',
                    description: 'Repointing and tuckpointing specialists',
                    technologies: 'WordPress website',
                    link: 'brickrestorations.com.au',
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'AusIMM',
                    description: 'The Australasian Institute of Mining and Metallurgy',
                    technologies: 'Optimizely, WordPress and static websites',
                    link: 'ausimm.com',
                    image: 'jonahhill.jpg'
                },
                {
                    title: 'PM Group',
                    description: 'PM Automotive Group',
                    technologies: 'WordPress, WebEd, Joomla, Cobalt and static websites',
                    link: 'pmgroup.com.au',
                    image: 'jonahhill.jpg'
                }
            ]
        }
    }

}
</script>

<style>

</style>