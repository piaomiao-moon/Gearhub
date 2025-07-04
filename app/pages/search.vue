<script setup lang="ts">
const route = useRoute()
const query = route.query.query as string
</script>

<template>
    <div style="text-align: center; margin-top: 100px">
        <h2>Result£º{{ query }}</h2>
        <p>(Find Result)</p>
    </div>
</template>
