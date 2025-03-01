<template>
  <main>
    <div class="row">
    sdfd
      <Input v-model="name"></Input>
      <Button>Submit</Button>
    </div>
    <div>
      <Table></Table>
    </div>

    <!-- <form class="row" @submit.prevent="greet">
      <input  v-model="name" placeholder="Enter a name..." />
      <button type="submit">Greet</button>
    </form>
    <p>{{ greetMsg }}</p> -->
  </main>
</template>
<script setup>
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/core";

import Button from "./Components/Button.vue";
import Input from "./Components/Input.vue";
import Table from "./Components/Table.vue";

const greetMsg = ref("");
const name = ref("");

async function greet() {
  // Learn more about Tauri commands at https://tauri.app/develop/calling-rust/
  greetMsg.value = await invoke("greet", { name: name.value });
}
</script>
<style scoped lang="sass">
.row
  display: flex
  align-items: center
  gap: 0.5em

.logo
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: 0.75s;
  &:hover
    filter: drop-shadow(0 0 2em #747bff)
</style>
<style>
:root {
  font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 24px;
  font-weight: 400;

  color: #0f0f0f;
  background-color: #f6f6f6;

  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  -webkit-text-size-adjust: 100%;
}

@media (prefers-color-scheme: dark) {
  :root {
    color: #f6f6f6;
    background-color: #2f2f2f;
  }

  a:hover {
    color: #24c8db;
  }

  input,
  button {
    color: #ffffff;
    background-color: #0f0f0f98;
  }
  button:active {
    background-color: #0f0f0f69;
  }
}

</style>
