<script>
  import Modal from '../components/Modal';

  export default {
    name: 'index',
    components: {
      Modal,
    },
    data () {
      return {
        isModalVisible: false,
      };
    },
    methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    },
  };
</script>

<template>
  <div id="index">
    <button
      type="button"
      @click="showModal"
    >
      Open Modal
    </button>

    <Modal
      v-show="isModalVisible"
      @close="closeModal"
    />
  </div>
</template>