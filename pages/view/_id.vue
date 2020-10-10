<template>
    <div>
        <div :class="$style.container" v-for="item of items" :key="item.id">
            <div>
                <img :class="$style.image" :src="item.image" alt="">
            </div>
            <div :class="$style.info">
                <div :class="$style.nameContainer">
                    <div :class="$style.name">{{item.name}}</div>
                        &nbsp;
                    <div :class="$style.nameType">«{{item.type}}»</div>
                </div>

                <div>
                    
                    
                </div>

                <Features />

                <Rent>
                    {{item.rent}}
                </Rent>
            </div>
        </div>
        
    </div>
</template>

<script>
import Rent from '@/components/Rent'
import Features from '@/components/Features'
import DataItems from '@/static/data.json'
export default {
    async asyncData({params}){
    const items = await DataItems.filter(el => el.id === params.id)
    return {items}
    }
}
</script>

<style module lang="css" scoped>
  
    .image{
        width: 100%;
        height: auto;
        border-radius: 24px;
    }
    .container{
        display: flex;
    }
    .nameContainer{
        display: flex;
        font-size: 40px;
        font-weight: bold;
        margin-bottom: var(--base);
    }
    .nameType::first-letter{
        text-transform: uppercase;
    }
    .info{
        width: 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-left: 65px;
    }

    @media (max-width: 1100px) {
        .container{
            padding: 0 16px;
            flex-direction: column;
            height: calc(100vh + 100px);
        }
        .info{
          margin: 0;
          margin-top: 22px;
          width: 100%;
        }
        .nameContainer{
            font-size: 24px;
            margin-bottom: 16px;
        }
     }

</style>