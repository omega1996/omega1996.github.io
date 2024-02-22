<template>
    <span @mouseover="showHint = true" @mouseleave="showHint = false" class="hint">
        <slot></slot>
        <Transition>
            <div class="hint__box" v-if="showHint">
                {{ text }}
                <slot name="hint"></slot>
            </div>
        </Transition>
    </span>
</template>

<script setup lang='ts'>
import { ref } from 'vue';

type Props = {
    text?: string
}

defineProps<Props>()

const showHint = ref(false)

</script>

<style scoped lang='scss'>
.v-enter-active,
.v-leave-active {
    transition: opacity 0.15s ease 0.3s;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}

.hint {
    position: relative;

    cursor: pointer;

    &__box {
        position: absolute;
        bottom: 20px;
        left: -20px;
        min-width: 200px;
        background: #252526;
        border: 1px solid grey;
        border-radius: 3px;
        padding: 0.4em;
        color: grey;
    }
}
</style>