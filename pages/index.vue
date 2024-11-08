<script setup>
import api from '~/data/api.json';
const { data: apis } = await useFetch('/api/learn');
debugger
</script>

<template>
    <div>
      <div v-if="!apis">Loading...</div>
      <div v-else>
        <div v-for="api in apis" :key="api.name">
            <p> Id: {{ api.id }}</p>
          <p>Name: {{ api.name }}</p>
          <p>Age: {{ api.age }}</p>
          <p>Email: {{ api.email }}</p>
          <p>Address: {{ api.address.street }}, {{ api.address.city }}, {{ api.address.state }} {{ api.address.zip }}</p>
        </div>
      </div>
    </div>
  </template>
  
