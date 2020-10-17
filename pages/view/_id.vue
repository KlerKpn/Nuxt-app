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

                <div :class="$style.tabs">
                    <nav :class="$style.nav">
                        <div :class="$style.navItem" id='1' @click.prevent="openTab($event)" style='color:#4959FF;'>
                            Specifications
                        </div>
                        <div :class="$style.navItem" id='2' @click.prevent="openTab($event)">
                            Team
                        </div>
                        <div :class="$style.navItem" id='3' @click.prevent="openTab($event)">
                            Rent terms
                        </div>
                    </nav>

                    <div>
                        <label v-show='true' for="1">
                            <Features />
                        </label>
                        <label v-show='false' for="2">
                            <Team />
                        </label>
                        <label v-show='false' for="3">
                            <RentTerms />
                        </label>
                    </div>
                </div>

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
import Team from '@/components/Team'
import RentTerms from '@/components/RentTerms'
import DataItems from '@/static/data.json'
export default {
    async asyncData({params}){
    const items = await DataItems.filter(el => el.id === params.id)
        if(items.length > 1){
            throw new Error('items more than 1')
        } else {
            return {items}
        }
        
    },

    methods: {
        openTab: (event)=> {
            const id = event.target.id
            let lbls = document.getElementsByTagName('label')
            lbls.forEach(( el, index)=> {
                document.getElementsByTagName('label')[index].setAttribute('style', 'display:none;')
                document.getElementById(index+ 1).removeAttribute('style')
            })
            document.getElementsByTagName('label')[id-1].setAttribute('style', 'display:inline-block;')
            event.target.setAttribute('style', 'color:#4959FF;')
        }
    }
}
</script>

<style module lang="css" scoped>
    .tabs{
        margin-bottom:0;
    }
    .nav{
        display: flex;
        font-weight: bold;
        margin-bottom: var(--base);
    }
    .navItem{
        cursor: pointer;
        margin-right: var(--base);
    }
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
        width: 40%;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        margin-top: 65px;
        margin-left: 65px;
    }

    @media (max-width: 1100px) {
        .container{
            padding: 0 16px;
            flex-direction: column;
            height: calc(100vh + 400px);
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