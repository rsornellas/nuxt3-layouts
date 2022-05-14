<template>
  <div>
    <header>
      <slot name="header" />
    </header>

    <main>
      <slot />
    </main>

    <slot name="sponsors" />

    <slot name="about" />
    
    <slot name="footer" />
  </div>

</template>
