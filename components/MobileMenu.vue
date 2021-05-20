<template>
    <nav>
        <ul class="lg:hidden flex flex-wrap justify-center font-semibold tracking-widest">
            <li v-for="item in menuItems" :key="menuItems[item]">
                <a class="cursor-pointer" :class=" active == item.link ? 'active' : '' " @click="menu(item.link)">{{ item.name }}</a>
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

a.active {
    text-decoration: underline;
}
</style>