<script setup lang="ts">
import { ref } from "vue";
import { ElMessage } from "element-plus";

defineProps<{ msg: string }>();

const count = ref(0);

const alertMsg = () => {
  ElMessage.info("clicked");
};
</script>

<template>
  <h1 @click="alertMsg">{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p class="color-pink font-100 m-y-0 pl-10 font-mono">
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p color="pink" font="100 mono" m="y-0">
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
