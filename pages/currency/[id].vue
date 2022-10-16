<script setup>
const route = useRoute()
const {data} = await useFetch('/api/ticker/?id=' + route.params.id, {key: `/currency/${route.params.id}`})
const coin = data.value[0]
</script>

<template>
    <main>
        <h2>{{coin.name}} Details</h2>
        <table>
            <thead>
                <th>Symbol</th>
                <th>Rank</th>
                <th>Price (US$)</th>
                <th>Market Cap (US$)</th>
                <th>% Change (24hrs)</th>
            </thead>
            <tr>
                <td>{{coin.symbol}}</td>
                <td>{{coin.rank}}</td>
                <td>{{coin.price_usd}}</td>
                <td>{{coin.market_cap_usd}}</td>
                <td>{{coin.percent_change_24h}}</td>
            </tr>
        </table>
    </main>
</template>