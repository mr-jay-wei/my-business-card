<script setup>

</script>

<template>
  <main class="card-container">
    <div class="card">
      <h1 class="name"> 大拿 </h1>
      <h1 class="title"> 世界顶级的美股投资操盘手 & AI工程师 </h1>
      <p class="quote"> “让数据驱动决策，让代码创造价值。” </p>
    </div>
  </main>
  <RouterView />
</template>

<style scoped>
  .card-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f2f5;
    font-family: 'Segoe UI', sans-serif;
  }
  .card {
    padding: 40px;
    border-radius: 15px;
    background-color: white;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
  }
  .name {
    margin: 0;
    font-size: 2.5em;
    color: #333;
  }
  .title {
    margin: 10px 0 20px;
    font-size: 1.2em;
    color: #007bff;
    font-weight: normal;
  }
  .quote {
    margin: 0;
    font-size: 1em;
    color: #666;
    font-style: italic;
  }
</style>
