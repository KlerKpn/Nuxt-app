<template>
    <div :class="$style.item" >
        <slot />
    </div>
</template>


<style module lang="css" scoped>
    .item{
        background: #FCFCFC;
        cursor: pointer;
        /* height: 100px; */
    
        color: black;
        border-radius: 32px;
        display: flex;
        padding: 24px 32px;
        /* margin: 3%; */
    }
</style>