<template>
  <div class="accordion" :class="{ 'accordion--opened': opened }" @click="opened = !opened">
    <img src="../assets/chevron-down.svg" class="accordion__chevron" :class="{ 'accordion__chevron--opened': opened }"
      width="13" height="13" alt="">
    {{ title }} <span class="accordion__comment" v-if="comment"> // {{ comment }}</span>
    <div class="accordion__container" :class="{ 'accordion__container--opened': opened }">
      <div class="accordion__container--inner">

        <slot></slot>
      </div>
    </div>
  </div>
</template>


<script setup lang="ts">
import { ref } from 'vue';


const opened = ref(false)

type Props = {
  title: string,
  comment?: string
}

defineProps<Props>()

</script>

<style lang="scss" scoped>
.accordion {
  cursor: pointer;

  &__comment {
    color: #6A9955;
  }

  &__container {
    display: grid;
    grid-template-rows: 0fr;
    overflow: hidden;
    transition: grid-template-rows 0.2s ease-in-out, margin-top 0.2s ease-in-out, opacity 0.2s ease-in-out;

    margin-top: 0px;
    opacity: 0;

    &--opened {
      grid-template-rows: 1fr;
      opacity: 1;
    }

    &--inner {
      overflow: hidden;
    }
  }

  &__chevron {
    transform: rotate(-90deg);
    transition: transform 0.2s ease-in-out;

    &--opened {
      transform: rotate(0deg);
    }
  }
}
</style>