<template>
  <div class="modal" v-if="store.isEditModalVisible">
    <div class="modal-content">
      <AdminProductEditForm />
    </div>
  </div>

</template>

<script setup>
import AdminProductEditForm from '@/admin/components/AdminProductEditForm.vue';
import { useAdminStore } from '@/stores/admin';

const store = useAdminStore()

</script>

<style scoped>
.modal {
  display: block;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.4);
}

.modal-content {
  background-color: #fefefe;
  padding: 20px;
  border: 1px solid #888;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: auto;
  max-width: 600px;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}
</style>
