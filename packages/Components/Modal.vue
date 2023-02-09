<script setup>
const props = defineProps({
  isShow: {
    type: Boolean,
    default: false,
  },
  hasCloseButton: {
    type: Boolean,
    default: true,
  },
});
const emit = defineEmits(['close']);
</script>

<template>
  <div class="modal" v-if="isShow">
    <div class="modal__content" @click="$emit('close')">
      <span class="modal__close-btn" v-if="hasCloseButton">&times;</span>
      <slot />
    </div>
  </div>
</template>

<style scoped lang="scss">
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 999;
}
.modal__close-btn {
  position: absolute;
  display: block;
  top: -15px;
  right: -15px;
  font-size: 20px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  text-align: center;
  background-color: #fff;
  border-radius: 50%;
  border: 1px solid #eee;
  cursor: pointer;
  z-index: 100;
}

.modal__content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
}
</style>