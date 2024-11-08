<script setup>
    const {data} = await useFetch('/api/learn')
</script>

<template>
    <div>
        <h1>
            Playing with Nuxt-Server. 
        </h1>
        <p>
            Json Data from server is: {{ data }}
        </p>
    </div>
</template>