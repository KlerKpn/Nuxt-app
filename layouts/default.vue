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
:root{
  --base :32px;
  --base-color:#012345;
  --base-background: #FCFCFC;
}
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

  background: var(--base-background);
  color: var(--base-color);
  padding: 3%;
  max-width: 1920px;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
