<template>
    <a :href="'//' + link" target="_blank" :style="{ backgroundImage: backGround}">
        
        <div class="text text-white p-6">
            <h3 class="text-2xl">{{ title }}</h3>
            <h4 class="text-lg">{{ description }}</h4>
            <h5 class="text-base mt-2">{{ technologies }}</h5>
        </div>

    </a>
</template>

<script>
export default {
    props: ['link', 'title', 'image', 'description', 'technologies'],
    data() {
        return {
            backGround: `url(` + require(`~/assets/images/${this.image}`) + `)`
        }
    }
}
</script>

<style scoped>

a {
    position: relative;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-color: rgb(0,0,0, 0.5);
    background-blend-mode: multiply;
    transition: all .4s;
}

a:hover, a:focus {
    background-size: cover;
    background-color: #fff;
    transition: background-color .4s ease-in;
}

.text {
    position: absolute;
    bottom: 0;
    left: 0;
}
</style>