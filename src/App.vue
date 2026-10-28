<script setup>
import { RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";
import Sidebar from "./components/Sidebar.vue";
import Dashboard from "./components/Dashboard.vue";
</script>

<template>
  <RouterView />
  <Navbar />
  <Sidebar />
  <Dashboard />
</template>
