<template>
  <div class="card">
    <h1>{{ title }}</h1>
    <button class="bth" @click="navigate">Открыть пользователя</button>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from "vue";
  import { useRouter } from "vue-router";

  export default defineComponent({
    setup() {
      const router = useRouter();
      return {
        title: "Vue",
        navigate: () => router.push("/users"),
      };
    },
  });
</script>
