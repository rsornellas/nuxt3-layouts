<template>
  <div class="container">
    <div class="sidebar">
      <slot name="sidebar" />
    </div>
    
    <div class="content">
      <header>
        <slot name="header" />
      </header>

      <slot name="about" />

      <slot name="sponsors" />

      <slot />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
}

.content {
  width: 100%;
}

.sidebar {
  width: 400px;
  max-height: 100%;
}
</style>
