<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <button type="button" @click="store.count++">
      pinia count is {{ store.count }}
    </button>
    &emsp;
    <n-button quaternary circle>
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <n-button quaternary circle type="primary">
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <n-button quaternary circle type="info">
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <n-button quaternary circle type="success">
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <n-button quaternary circle type="warning">
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <n-button quaternary circle type="error">
      <template #icon>
        <n-icon><cash-icon /></n-icon>
      </template>
    </n-button>
    <p>
      Thank you for use llx-cli !
      <code></code>Development by 刘兴
    </p>
  </div>

  <p>
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

<script setup lang="ts">
import { ref } from "vue";
import { CashOutline as CashIcon } from "@vicons/ionicons5";
import { useCountStore } from "../store/modules/count";

defineProps<{ msg: string }>();

const store = useCountStore();

const count = ref(0);
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
