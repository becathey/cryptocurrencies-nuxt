<script setup>
const {data} = await useFetch('/api/tickers/?limit=10')
const result = data.value
console.log(result)
</script>

<template>
    <main>
        <h1>Top 10 Ranked Cryptocurrency Coins</h1>
        <table border="1px solid">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Symbol</th>
                    <th>Price</th>
                    <th>Details</th>
                </tr>
            </thead>
            <tr v-for="currency in data.data" :key="currency.id">
                <td>{{currency.name}}</td>
                <td>{{currency.symbol}}</td>
                <td>{{currency.price_usd}}</td>
                <td>
                    <NuxtLink :to="'/currency/' + currency.id">
                    {{currency.id}}
                    </NuxtLink>
                </td>
            </tr>
        </table>
    </main>
</template>