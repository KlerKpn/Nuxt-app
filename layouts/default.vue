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
  --base-table: #F3F4F7;
  --base-descColor:#677B8F;
  --blue: #4959FF;
}
.darkmode{
  --base-color:#FCFCFC;
  --base-background: #012345;
  --base-table: #011C37;
  --base-descColor: #99A7B5;
}
.layout {
  font-family:
    'Codec Pro News',
    'Source Sans Pro',
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  line-height: 20px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;

  background: var(--base-background);
  color: var(--base-color);
  padding: 4%;
  padding-top: 0;
  max-width: 1920px;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
@media (max-width: 1100px) {
  .layout{
    padding:0;
  }
}
</style>
