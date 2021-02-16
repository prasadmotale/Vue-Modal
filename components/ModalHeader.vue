<script>
  export default {
    name: 'ModalHeader',

    methods: {
      closeModal() {
        this.$emit('closeModal');
      },
    },
  };
</script>

<template>
    <div class="modal-header">
        <h2>Register</h2>
        <slot name="header">
          <button
            type="button"
            class="btn-close"
            @click="closeModal"
          >
            x
          </button>
        </slot>
    </div>
</template>

<style scoped>
.modal-header button{
    left: 5px;
    top: 0px;
    position: relative;
}
.h2{
    text-align: center;
}
</style>