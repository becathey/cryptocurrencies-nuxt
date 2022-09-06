<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: hsl(210, 90%, 95%);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
main {
  margin-top: 1rem;
  display: grid;
  justify-content: center;
  align-items: center;
  color: hsl(230, 20%, 40%);
  font-size: 0.9rem;
}
h1 {
  font-size: 1.5rem;
  text-align: center;
}
h2 {
  font-size: 1.25rem;
  text-align: center;
}
table {
  border-collapse: collapse;
  background-color: white;
  box-shadow: 20px 20px 20px 5px hsl(210, 30%, 70%);
  margin-bottom: 2rem;
}
th {
  background-color: hsl(210, 60%, 90%);
  padding: 0.75rem 1rem;
  text-align: center;
  font-size: 0.7rem;
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.1rem;
}
td {
  padding: 1rem;
  text-align: center;
}
tr:nth-child(even) {
  background-color: hsl(210, 90%, 95%);
}
</style>