<template>
<div class="placeholder" :style="styles">
    <div v-if="icon !== ''" class="placeholder-icon">
        <icon :name="icon"/>
    </div>
    <div v-if="!!$slots.default" class="placeholder-content">
        <slot></slot>
    </div>
</div>
</template>

<script>
export default {
    props: {
        icon: { type: String, default: '' },
        height: { type: [String, Number], default: 256 },
        color: { type: String, default: '#DDD' },
    },
    computed: {
        styles() {
            return {
              'min-height': this.height + 'px',
              'background-color': this.color,
            }

         }
    }
}
</script>

<style>
.placeholder {
    position: relative; border-radius: 0;
    color: #FF5D25;
    border-bottom: 2px solid #122035;
}



.placeholder-icon {
    position: absolute; top: 40%; left: 40%;
    width: 64px; height: 64px; line-height: 64px;
    margin-top: -32px; margin-left: -32px;
    font-size: 100px;

}
</style>
