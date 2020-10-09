<template>
    <div :class="$style.main">
        <div :class="$style.row">
            <div :class="$style.row">
                <div>Rent for</div>
                    &nbsp;
                <div :class="$style.rent">
                    <slot /> $/h
                    </div>
            </div>
            <button :class="$style.btn">
                Rent now
            </button>
        </div>
    </div>
</template>

<style module lang="css" scoped>
    .main{
        width: 100%;
        height: 80px;
        display: flex;
        justify-content: space-between;
        border-radius: 16px;
        background: #F3F4F7;
        font-weight: bold;
        padding: 16px 32px;
    }
    .row{
        width: 100%;
        display: flex;
        align-items: center;
        font-size: 20px;
    }
    .rent{
        color: #F84AB3;
    }
    .btn{
        display: flex;
        white-space: nowrap;
        height: 44px;
        justify-content: center;
        align-items: center;
        background: #4959FF;
        padding: 17px 32px;
        border-radius: 12px;
        border: none;
        outline: none;
        color: #FCFCFC;
        font-weight: bold;
        cursor: pointer;
    }
</style>