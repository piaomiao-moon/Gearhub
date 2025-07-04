<script setup lang="ts">
const route = useRoute()
const query = route.query.query as string
</script>

<template>
    <div style="text-align: center; margin-top: 100px">
        <h2>搜索结果：{{ query }}</h2>
        <p>（这里可展示真实搜索结果，或调用后端 API 获取）</p>
    </div>
</template>
