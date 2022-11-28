<template>
  <div class="toast">
    <div class="toast-icon">
      <IconSuccess />
    </div>
    <div class="toast-content">
      <div class="toast-title">Success</div>
      <div class="toast-message">Data has been saved</div>
    </div>
    <button class="toast-button">&times;</button>
  </div>
</template>

<script>
  import IconError from './IconError.vue';
  import IconWarning from './IconWarning.vue';
  import IconSuccess from './IconSuccess.vue';

  export default {
    components: {
      IconError,
      IconWarning,
      IconSuccess,
    }
  }

</script>

<style scoped lang="css">
.toast {
  width: 300px;
  background-color: #ecfdf5;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  box-shadow: 1px 5px 10px -5px rgba(0, 0, 0, 0.2);
  position: relative;
}

.toast::before {
  content: "";
  width: 4px;
  height: 100%;
  background-color: #34d399;
  position: absolute;
  top: 0;
  left: 0;
}

.toast-icon {
  width: 16px;
  height: 16px;
  background-color: #34d399;
  border-radius: 50%;
  padding: 7px;
}

.toast-icon svg {
  fill: #ecfdf5;
}

.toast-content {
  flex-grow: 1;
  margin: 0 1rem;
}

.toast-title {
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.toast-message {
  font-size: 14px;
  color: #6b7280;
}

.toast-button {
  width: 1.5rem;
  height: 1.5rem;
  border: none;
  padding: 0;
  color: #9ca3af;
  opacity: 0.7;
  background-color: transparent;
  cursor: pointer;
  font-size: 1rem;
}

.toast-button:hover {
  opacity: 1;
}


</style>