<template>
  <div :class="$style.layout">
    <Header />
      <main>

        <nuxt />
        
      </main>
  </div>
</template>

<script>
import Header from '@/components/Header'
export default {

}
</script>

<style module lang='css'>
.layout {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;

  color: #012345;
  padding: 3%;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
