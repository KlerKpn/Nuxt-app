<template>
    <div :class="$style.item" >
        <slot />
    </div>
</template>


<style module lang="css" scoped>
    .item{
        background: #FCFCFC;
        cursor: pointer;
        height: 164px;
        border-radius: 32px;
        display: flex;
        padding: 24px 32px;
    }
</style>