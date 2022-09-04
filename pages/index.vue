<script setup>
const {data} = await useFetch('/api/tickers/?limit=10')
const result = data.value
</script>

<template>
    <main>
        <h1>Top 10 Cryptocurrencies</h1>
        <table>
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