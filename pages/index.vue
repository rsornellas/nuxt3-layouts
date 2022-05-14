<template>
  <NuxtLayout :name="layout">
    <template #header>
      <section class="header">HEADER</section>
    </template>

    <template #about>
      <section class="about">ABOUT</section>
    </template>

    <template #sponsors>
      <section class="sponsors">SPONSORS</section>
    </template>

    <section class="main">MAIN CONTENT</section>

    <template #footer>
      <section class="footer">FOOTER</section>
    </template>

    <template #sidebar>
      <section class="sidebar">SIDEBAR</section>
    </template>
  </NuxtLayout>

  <div class="buttons">
    <h3>Current layout: {{ layout }}</h3>

    <button :disabled="layout === 'customa'" @click="change('customa')">Change to layoutA</button>
    <button :disabled="layout === 'customb'" @click="change('customb')">Change to layoutB</button>
    <button :disabled="layout === 'customc'" @click="change('customc')">Change to layoutC</button>
  </div>
</template>

<script setup>
const layout = ref("customa");

const change = (layoutName) => {
  layout.value = layoutName;
};
</script>

<style scoped>
button {
  margin-left: 10px;
  padding: 15px 15px 15px 15px;
}

section {
  font-size: 22px;
  font-weight: bold;
  height: 60px;
  align-items: center;
  display: flex;
  justify-content: center;
}
.buttons {
  display: content;
  padding: 10px 0 0 100px;
}
.header {
  background-color: red;
}
.about {
  background-color: blue;
}
.sponsors {
  background-color: green;
}
.main {
  background-color: grey;
}
.footer {
  background-color: pink;
}
.sidebar {
  background-color: yellow;
  height: 100%;
}
</style>

<style>
body {
  margin: 0;
}
</style>
