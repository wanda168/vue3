<template>
  <div class="btns">
    <button @click="showTopLeftToast = true">Show Top Left Toast</button>
    <button @click="showTopRightToast = true">Show Top Right Toast</button>
    <button @click="showBottomLeftToast = true">Show Bottom Left Toast</button>
    <button @click="showBottomRightToast = true">Show Bottom Right Toast</button>
  </div>
  <Toast
    message="Message has been sent"
    :show="showTopLeftToast"
    @hide="showTopLeftToast = false"
    type="success"
    position="top-left"
  />
  <Toast
    message="Message has been sent"
    :show="showTopRightToast"
    @hide="showTopRightToast = false"
    type="warning"
    position="top-right"
  />
  <Toast
    message="Message has been sent"
    :show="showBottomLeftToast"
    @hide="showBottomLeftToast = false"
    type="error"
    position="bottom-left"
  />
  <Toast
    message="Message has been sent"
    :show="showBottomRightToast"
    @hide="showBottomRightToast = false"
    type="success"
    position="bottom-right"
  />
</template>

<script>
import Toast from "./components/toast/Toast.vue";
export default {
  components: { Toast },
  data: () => ({
      showTopLeftToast: false,
      showTopRightToast: false,
      showBottomLeftToast: false,
      showBottomRightToast: false,
  }),
};
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

.btns {
  margin: 10px 15%;
  display: flex;
  padding: 15% 10px;
  justify-content: space-between;
}

.btns button:hover {
  cursor: pointer;
}

</style>
