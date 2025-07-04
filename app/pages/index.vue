<script setup lang="ts">
const runtimeConfig = useRuntimeConfig()
const colors = ['#f87171', '#fb923c', '#fbbf24', '#facc15', '#a3e635', '#4ade80', '#34d399', '#2dd4bf', '#22d3ee', '#38bdf8', '#60a5fa', '#818cf8', '#a78bfa', '#c084fc', '#e879f9', '#f472b6', '#fb7185']
const color = useState('color', () => colors[Math.floor(Math.random() * colors.length)])

const search = ref('')
const router = useRouter()

function handleSearch() {
  if (search.value.trim()) {
    router.push(`/search?query=${encodeURIComponent(search.value)}`)
  }
}
</script>

<template>
    <div class="centered">
        <h1 :style="{ color }">
            {{ runtimeConfig.public.helloText || 'Welcome to GearHub' }}
        </h1>
        <input v-model="search" type="text" placeholder="ÇëÊäÈëÁã¼þ¹Ø¼ü´Ê" @keydown.enter="handleSearch" />
        <button @click="handleSearch">ËÑË÷</button>
    </div>
</template>

<style scoped>
    .centered {
        text-align: center;
        margin-top: 10%;
    }

    input {
        padding: 8px;
        font-size: 16px;
        margin-right: 8px;
    }

    button {
        padding: 8px 16px;
        font-size: 16px;
        cursor: pointer;
    }
</style>
