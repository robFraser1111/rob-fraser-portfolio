<template>
    <section class="cards">
        <CardSquare v-for="item in items" :key="items[item]" 
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
                    image: 'roo-digital-card-01.jpg'
                },
                {
                    title: 'Miiesha',
                    description: 'ARIA award winning R&B artist',
                    technologies: 'Vue website',
                    link: 'miiesha.com',
                    image: 'miiesha-card-01.jpg'
                },
                {
                    title: 'Joseph Vea',
                    description: 'New Zealand born, Tongan singer/songwriter',
                    technologies: 'React website',
                    link: 'josephvea.com',
                    image: 'joe-vea-card-01.jpg'
                },
                {
                    title: 'SS Bricklaying',
                    description: 'Local bricklaying company',
                    technologies: 'WordPress website',
                    link: 'ssbricklaying.melbourne',
                    image: 'ss-bricklaying-card-01.jpg'
                },
                {
                    title: 'Brick Restorations Melbourne',
                    description: 'Repointing and tuckpointing specialists',
                    technologies: 'WordPress website',
                    link: 'brickrestorations.com.au',
                    image: 'brick-restorations-card-01.jpg'
                },
                {
                    title: 'AusIMM',
                    description: 'The Australasian Institute of Mining and Metallurgy',
                    technologies: 'Optimizely, WordPress and static websites',
                    link: 'ausimm.com',
                    image: 'ausimm-card-01.jpg'
                },
                {
                    title: 'PM Group',
                    description: 'PM Automotive Group',
                    technologies: 'WordPress, WebEd, Joomla, Cobalt and static websites',
                    link: 'pmgroup.com.au',
                    image: 'pm-group-card-01.jpg'
                }
            ]
        }
    }

}
</script>

<style scoped>
.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, 32rem);
    justify-content: center;
}
</style>