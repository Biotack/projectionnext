<script lang="ts" setup>
const {data: brands, error, status } = await useFetch('/api/brands', {lazy: true,});

</script>


<template>
    <h1>
        <article v-if="status === 'pending'" :aria-busy="true"/>
        <article v-else-if="error" class="error" >
        {{ error.message }}
        </article>
        <div v-else>
        <article v-for="brand in brands" :key="brand.id">
            <h2>{{ brand.brandName }}</h2>
            <p>{{ brand.brandNumber}}</p>
            <!-- <NuxtLink :to="{ name: 'brand', params: { id: brand.id } }">View Details</NuxtLink> -->

        </article>
    </div>
    </h1>
</template>