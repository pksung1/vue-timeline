<template>
  <transition name="timeline-item-transtion" appear>
      <slot></slot>
  </transition>
</template>

<script>
export default {
    name: 'timeline-item-transtion'
}
</script>

<style lang="scss" scoped>
    .timeline-item-transtion-enter-active {
        animation: item-animation 0.5s;
    }
    .timeline-item-transtion-leave-active {
        animation: item-animation 0.5s reverse;
    }
    @keyframes item-animation {
        0% {
            transform: translateY(20px);
            opacity: 0;
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
</style>