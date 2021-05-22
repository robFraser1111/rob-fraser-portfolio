<template>
    <section class="logo text-center">
        <h1>
            Rob Fraser
        </h1>
        <h2 class="text-6xl font-semibold tracking-widest">
            Portfolio
        </h2>
        <h3 class="text-2xl p-6">
            <span>&#129497;</span>
        </h3>
    </section>
</template>

<script>
export default {
    data() {
        return {
            hero: null,
            text: null,
            mouse: null,
            walk: 15
        }
    },
    methods: {
        shadow(e) {
            const width = this.hero.offsetWidth;
            const height = this.hero.offsetHeight;

            let { offsetX: x, offsetY: y } = e;

            if (this != e.target) {
                x = x + e.target.offsetLeft;
                y = y + e.target.offsetTop;
            }

            const xWalk = Math.round((x / width * this.walk) - (this.walk / 2));
            const yWalk = Math.round((y / height * this.walk) - (this.walk / 2));

            this.text.style.textShadow = `${xWalk}px ${yWalk}px 0 rgb(191, 23, 132, 0.8)`
        }
    },
    mounted: function() {
        this.hero = document.querySelector('.hero');
        this.text = document.querySelector('.logo');
        this.mouse = this.hero.addEventListener('mousemove', this.shadow);
    }
}
</script>


<style scoped>
h1 {
    font-family: Boostpest;
    font-size: 12rem;
}
section {
    color: #fff;
    
}

@media only screen and (max-width: 720px) {
  h1 {
    font-size: 8rem;
  }
  h2 {
      font-size: 3rem;
  }
}
</style>