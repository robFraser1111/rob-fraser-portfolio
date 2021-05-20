<template>
    <a class="m-1" :href="'//' + link" target="_blank">

        <article>
            <div class="card" :style="{ backgroundImage: backGround}"></div>
                <div class="text text-white p-6">
                    <h3 class="text-2xl">{{ title }}</h3>
                    <h4 class="text-lg">{{ description }}</h4>
                    <h5 class="text-base mt-2">{{ technologies }}</h5>
                </div>
        </article>

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
    overflow: hidden;
}

article {
    width: 28rem;
    height: 42rem;
    overflow: hidden;
    position: relative;
}

.card {
    width: 100%;
    height: 100%;
    background-size: cover;
    background-position: center;
    background-color: rgb(0,0,0, 0.5);
    background-blend-mode: multiply;
    transition: all .4s;
}
.card:hover, .card:focus {
    transform: scale(1.2)
}

.text {
    position: absolute;
    bottom: 0;
}
</style>