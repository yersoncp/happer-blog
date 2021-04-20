<template>
  <header class="header font">
    <g-link to="/"><h1>{{siteName}} 🚀</h1></g-link>
    <ClientOnly>
      <ThemeToggle />
    </ClientOnly>
  </header>
</template>

<script>
export default {
  props: ["siteName"],
  components: {
    ThemeToggle: () => import('@/components/ThemeToggle')
  }
};
</script>

<style lang="scss">
  .header {
    display:flex;
    align-items: center;
    justify-content: space-between;
    a {
      color:inherit;
      border-bottom: none;
    }
  }
</style>
