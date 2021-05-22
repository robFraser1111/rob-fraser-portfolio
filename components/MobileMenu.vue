<template>
    <nav class="py-6">
        <ul class="lg:hidden flex flex-wrap justify-center font-semibold tracking-widest">
            <li class="mx-4 my-2" v-for="item in menuItems" :key="menuItems[item]">
                <a class="underline-from-left cursor-pointer" :class=" active == item.link ? 'active' : '' " @click="menu(item.link)">{{ item.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            active: 'Home'
        }
    },
    props: {
        menuItems: Array
    },
    methods: {
        menu(section) {
            this.$parent.changeSection(section);
            this.active = section
        }
    }
}
</script>

<style scoped>
nav {
    color: #fff;
}

.underline-from-left.active:before {
    content: "";
    position: absolute;
    z-index: -1;
    left: 0;
    right: 0;
    bottom: 0;
    background: #fff;
    height: 3px;
}
.underline-from-left:hover:before, .underline-from-left:focus:before, .underline-from-left:active:before {
    right: 0;
}
.underline-from-left {
    display: inline-block;
    vertical-align: middle;
    -webkit-transform: perspective(1px) translateZ(0);
    transform: perspective(1px) translateZ(0);
    box-shadow: 0 0 1px rgb(0 0 0 / 0%);
    position: relative;
    overflow: hidden;
}
.underline-from-left:before {
    content: "";
    position: absolute;
    z-index: -1;
    left: 0;
    right: 100%;
    bottom: 0;
    background: #fff;
    height: 3px;
    -webkit-transition-property: right;
    transition-property: right;
    -webkit-transition-duration: 0.3s;
    transition-duration: 0.3s;
    -webkit-transition-timing-function: ease-out;
    transition-timing-function: ease-out;
}
</style>