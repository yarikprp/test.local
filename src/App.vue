<template>
  <header class="navbar">
    <h3>Vue + TS</h3>
    <Ul class="navbar">
      <li>
        <router-link to="/">Главная</router-link>
      </li>
      <li>
        <router-link to="/users">Пользователи</router-link>
      </li>
    </Ul>
  </header>
  <main class="container with-nav">
    <router-view/>
  </main>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    methods: {
      workWithStore() {
        this.$store.state
      }
    }
  })
</script>