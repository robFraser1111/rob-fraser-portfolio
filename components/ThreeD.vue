<template>
    <section class="cards">
        <CardWide v-for="item in items" :key="items[item]" 
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
                    title: 'Metal Gear Solid: The Twin Snakes',
                    description: '3D interactive walkthrough',
                    technologies: 'Unreal Engine, Blender and Quixel',
                    link: 'behance.net/gallery/40610715/Metal-Gear-Solid-The-Twin-Snakes-Cargo-Dock',
                    image: 'twin-snakes-01.jpg'
                },
                {
                    title: 'Sonos Play:3',
                    description: 'Redesign concept',
                    technologies: 'Blender and Adobe CC',
                    link: 'behance.net/gallery/35861709/New-Sonos-Play3-Idea',
                    image: 'sonos-play-3.jpg'
                },
                {
                    title: 'Sonos Play:1',
                    description: 'Redesign concept',
                    technologies: 'Blender and Adobe CC',
                    link: 'https://www.behance.net/gallery/40609467/New-Sonos-Play1-Idea',
                    image: 'sonos-play-1.jpg'
                }
            ]
        }
    }

}
</script>

<style scoped>
.cards {
    display: grid;
    grid-auto-rows: 32rem;
    grid-gap: 5px;
}
</style>