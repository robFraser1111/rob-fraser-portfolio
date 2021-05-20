<template>
        <nav class="hidden lg:block fixed font-semibold tracking-widest">
            <ul class="space-y-6">
                <li v-for="item in menuItems" :key="menuItems[item]">
                    <a class="underline-from-left cursor-pointer" :class=" active == item.link ? 'active' : '' " @click="menu(item.link)">{{ item.name }}</a>
                </li>
            </ul>
        </nav>
</template>

<script>
export default {
    data() {
        return {
            active: 'Home',
            menuItems: [
                {
                    link: 'Home',
                    name: 'Home',
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
                    name: '3D'
                },
                {
                    link: 'Contact',
                    name: 'Contact'
                }
            ],
        }
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
    top: 50%;
    left: 60px;
    transform: translate(-50%, -50%);
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