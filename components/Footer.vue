<template>
    
    <ul class="flex flex-wrap justify-center">
        <li v-for="social in socials" :key="socials[social]" class="p-6">
            <a :href="'//' + social.link" target="_blank">
                <font-awesome-icon :icon="[social.iconPrefix, social.icon]" :style="socialStyle"/>
            </a>
        </li>
        <li class="p-6">
            <a href="mailto:robfraserdesign@gmail.com">
                <font-awesome-icon icon="envelope" :style="socialStyle"/>
            </a>
        </li>
    </ul>
    
</template>

<script>
export default {
    data() {
        return {
            socials: [
                {
                    link: 'github.com',
                    iconPrefix: 'fab',
                    icon: 'github'
                },
                {
                    link: 'behance.com',
                    iconPrefix: 'fab',
                    icon: 'behance'
                },
                {
                    link: 'linkedin.com',
                    iconPrefix: 'fab',
                    icon: 'linkedin'
                }
            ],
            socialStyle: {
                color: 'white',
                fontSize: '1.5rem'
            }
        }
    }
}
</script>

<style scoped>
a svg {
    transition: 0.3s;
    transform: scale(1);
}
a:hover svg, a:focus svg {
    transform: scale(1.2);
}
a:active svg {
    transform: scale(0.8);
}
</style>