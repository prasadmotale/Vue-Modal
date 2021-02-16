<script>
import ModalBody from "./ModalBody";
import ModalHeader from "./ModalHeader";
  export default {
    name: 'modal',

    methods: {
      close() {
        this.$emit('close');
      },
    },
  };
</script>

<template>
  <div class="modal-backdrop">
    <div class="modal">
      <div class="model-header">
          <ModalHeader @closeModal="close"/>
      </div>
      <div class="modal-body">
          <ModalBody/>
       </div>
       
       <div class="modal-footer">
          <slot name="footer">
            <button
              type="button"
              class="btn-close-foot"
              @click="close"
            >
              Close
            </button>

            <button
              type="button"
              class="btn-register"
              @click="close"
            >
              Register
          </button>
        </slot>
      </div>
    </div>
  </div>
</template>

<style>
  .modal-backdrop {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.3);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .modal {
    background: #FFFFFF;
    box-shadow: 2px 2px 20px 1px;
    overflow-x: auto;
    display: flex;
    flex-direction: column;
  }

  .modal-header,
  .modal-footer {
    padding: 15px;
    display: flex;
  }

  .modal-header {
    border-bottom: 1px solid #eeeeee;
    color: #4AAE9B;
    justify-content: space-between;
  }

  .modal-footer {
    border-top: 1px solid #eeeeee;
    justify-content: flex-end;
    padding: 20px;
    margin: 20px;
  }

  .modal-body {
    position: relative;
    padding: 20px 10px;
  }

  .btn-close {
    border: none;
    font-size: 20px;
    padding: 20px;
    cursor: pointer;
    font-weight: bold;
    color: #4AAE9B;
    background: transparent;
  }

 .btn-close-foot {
    color: white;
    background-color: #555555;
    border: none;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
  }
.btn-register{
    color: white;
    background-color:  #4AAE9B;
    border: none;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
}
</style>
