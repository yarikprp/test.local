<template>
  <ul class="list">
    <li class="list-item" v-for="user in users">
      {{ user.name }}
    </li>
  </ul>
</template>

<script lang="ts">
  import { useUsers } from "@/use/users";
  import { defineComponent } from "vue";

  export default defineComponent({
    async setup() {
      const { users } = await useUsers();
      return { users };
    },
  });
</script>
