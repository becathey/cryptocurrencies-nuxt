<template>
    <nav>
        <NuxtLink to="/">CryptoMonitor</NuxtLink>
    </nav>
    <main>
        <slot />
    </main>
</template>

<style scoped>
nav {
    background-color: hsl(210, 90%, 30%);
    padding: 1rem;
    font-variant: small-caps;
    font-size: 1.25rem;
}
nav a {
    text-decoration: none;
    color: white;
}
nav a:hover {
    border-bottom: 1px solid hsl(210, 90%, 95%);
}
</style>