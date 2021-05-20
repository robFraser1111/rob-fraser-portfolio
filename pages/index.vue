<template>

      <div class="hero main grid min-h-screen mx-auto px-4">

        <header class="h-24 self-start">
          <MobileMenu :menuItems="menuItems"/>
        </header>
        
        <main class="grid grid-cols-10 content-center gap-2">
    
          <div class="col-span-1 self-center">
            <Menu />
          </div>
            
          <div class="col-span-8">
            <transition name="fade" mode="out-in">
              <component :is="view"></component>
            </transition>
          </div>
      
        </main>

        <footer class="h-24 self-end">
          <Footer />
        </footer>

      </div>

</template>

<script>
import MobileMenu from '~/components/MobileMenu.vue'
export default {
  components: { MobileMenu },
  data() {
    return {
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
      view: 'Home'
    }
  },
  layout: 'default',
  methods: {
    changeSection(section) {
      this.view = section
    },
    moveDownPage(e) {
      if(e.key == 'ArrowDown') {
        console.log(this.view)
      }
    }
  },
  computed: {
    currentPage() {
      return this.view
    }
  },
  mounted() {
    window.addEventListener('keydown', (e) => {
      this.moveDownPage(e)
    })
  }
}
</script>

<style scoped>
  .main {
    max-width: 2560px;
  }
</style>

<style>

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s
}
.fade-enter, .fade-leave-active {
  opacity: 0
}

</style>
