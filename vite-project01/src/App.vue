<template>
  <div>
    <app-header v-bind=propsdata="str"></app-header>
  </div>
</template>

<script setup>
// 1. 우리가 만든 '헤더' 부품을 불러옵니다(import).
import AppHeader from './components/AppHeader.vue'
</script>

<style scoped>
main {
  padding: 20px;
  font-size: 1.2rem;
  text-align: center;
}
</style>