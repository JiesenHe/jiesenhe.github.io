<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

const navigateToBlog = () => {
  router.push({ name: 'home' })
}
</script>

<template>
  <div class="splash-page" @click="navigateToBlog">
    <div class="greeting-box">
      <h1>Hello World! 🌍</h1>
      <p>欢迎来到我的博客</p>
      <p class="hint">(点击任意位置进入博客)</p>
    </div>
  </div>
</template>

<style scoped>
.splash-page {
  background: linear-gradient(135deg, #89f7fe, #66a6ff);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  cursor: pointer;
}

.greeting-box {
  background: rgba(255, 255, 255, 0.9);
  padding: 2rem 4rem;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  text-align: center;
  animation: fadeIn 1s ease-in;
}

h1 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 2.5em;
}

p {
  color: #34495e;
  font-size: 1.2em;
  margin: 0;
}

.hint {
  margin-top: 1rem;
  font-size: 0.9em;
  color: #7f8c8d;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>