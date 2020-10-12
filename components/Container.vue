<template>
  <div :class="$style.container">
    <slot />
  </div>
</template>

<style module lang="css">
  .container{
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: center;  
    background:#F3F4F7;
    padding: 4%;
    border-radius: 48px;
    margin: 0 auto;
    min-height: 708px;
    justify-content: center;
  }
</style>
