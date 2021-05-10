<template>
    <div>
        <ul class="space-y-6">
            <li v-for="item in menuItems" :key="menuItems[item]">
                <a class="cursor-pointer" @click="menu(item.link)">{{ item.name }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            menuItems: [
                {
                    link: 'Home',
                    name: 'Home'
                },
                {
                    link: 'Web',
                    name: 'Web'
                },
                {
                    link: 'Design',
                    name: 'Design'
                },
                {
                    link: 'Print',
                    name: 'Print'
                },
                {
                    link: 'ThreeD',
                    name: '3d'
                }
            ]
        }
    },
    methods: {
        menu(section) {
            this.$parent.changeSection(section);
        }
    }
}
</script>