<template>
  <div>
    <div>
      <button @click="action">switch</button>
    </div>
    <transition name="fade" mode="in-out">
      <div v-show="fadeObject">hello world</div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fadeObject: true,
    }
  },
  methods: {
    action() {
      this.fadeObject = !this.fadeObject
    },
  },
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-in-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
