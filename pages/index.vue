<template>
    <div class="grid h-screen grid-cols-12 content-center gap-2">
  
      <div class="col-span-2">
        <Menu />
      </div>
        
      <div class="col-span-8">
        <transition name="fade" mode="out-in">
          <component :is="view"></component>
        </transition>
      </div>

      <div class="col-span-2">
        <!-- Space -->
      </div>
  
    </div>
</template>

<script>
export default {
  data() {
    return {
      view: 'Home'
    }
  },
  layout: 'default',
  methods: {
    changeSection(section) {
      this.view = section
    }
  }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
