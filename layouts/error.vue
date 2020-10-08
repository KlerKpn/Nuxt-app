<template>
    <div>
        <Container>
            <div :class="$style.errContainer">
                <div :class="$style.err">An error has occurred</div>
                <div :class="$style.description">Please refresh the page</div>
                <button :class="$style.errButton">Reload page</button>
            </div>
        </Container>
    </div>
</template>

<script>
import Container from '@/components/Container'
export default {}
</script>

<style module lang="css" scoped>
    .errContainer{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .err{
        font-size: 40px;
        font-weight: bold;
        margin-bottom: 16px;
    }
    .description{
        font-size: 14px;
        color: #677B8F;
        margin-bottom: 32px;
    }
    .errButton{
        font-weight: bold;
        background: #4959FF;
        border-radius: 12px;
        padding: 16px 24px;
        color: white;
        border: none;
    }   
    
</style>