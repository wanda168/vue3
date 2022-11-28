<template>
  <button @click="showToast = true">Show Toast</button>
  <Toast title="Yes" message="Message has been sent!" :show="showToast"/>
</template>

<script>
import Toast from "./components/toast/Toast.vue";

export default {
  components: { Toast },
  data: () => ({
    showToast: false
  })
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
