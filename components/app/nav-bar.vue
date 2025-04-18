<template>
<nav class="container">
    <ul>
        <li>
            <NuxtLink to="/">
                <strong>VintPlan</strong>
            </NuxtLink>
        </li>
    </ul>
    <ul>
        <li>
            <NuxtLink :to="{ name:'brands' }">Brands</NuxtLink>
        </li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Products</a></li>
    </ul>
    </nav>
</template>