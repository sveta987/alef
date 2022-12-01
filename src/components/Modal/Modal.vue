<template>
  <transition name="modal">
    <div class="modal-mask" @click="$emit('close')">
      <div class="modal-wrapper">
        <div class="modal-container">
          <slot name="header">Header</slot>
          <button class="modal-default-button" @click="$emit('close')">Close</button>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "Modal",
}
</script>
<style src="./modal.css"></style>
