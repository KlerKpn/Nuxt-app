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
    @media (max-width: 1100px) {
        .item{
            padding: 20px 20px; 
            height: 151px;
        }
    }
    
</style>