<template>
  <div :class="$style.container">
    <Container>
      <div :class="$style.head">
          <div :class="$style.whatever">Rent <span :class="$style.whateverBlue">whatever</span></div>
          <div :class="$style.addNew"><span>Add new</span></div>
      </div>
      <div :class="$style.table">
        <Item v-for="item of items" :key="item.id" @click.native="openItem(item)">
          <div :class="$style.prevContainer">
                    <img :class="$style.imgPrev" :src='item.preview' alt="">
                </div>
                <div :class="$style.prevContent">
                    <div :class="$style.prevHead">
                        <div :class="$style.name">{{item.name}}</div>
                            &nbsp;
                        <div :class="$style.nameType">«{{item.type}}»</div>
                    </div>   
                    <p :class="$style.description">{{item.description}}</p>
                    <div :class="$style.rent">{{item.rent}} $/h</div>
                </div>
        </Item>
      </div>
    </Container>
  </div>
</template>

<script>
import Container from '@/components/Container'
import Item from '@/components/Item'
import DataItems from '@/static/data.json'

export default {
    data:()=>({
        items:[]
    }),
    mounted(){
        this.items = DataItems
    },
    methods:{
      openItem(item){
        console.log(item)
      }
    }   
}
</script>

<style module lang='css' scoped>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  text-align: center;
}
  .table{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(186px, 1fr));
    grid-gap: 32px;
  }
  .head{
    display: flex;
    width: 100%;
    justify-content: space-between;
    padding: 0 0 5% 0;
    font-weight: bold;
  }
    .whatever{
      font-size: 48px;
    }
      .whateverBlue{
        color: #4959FF;
      }
    .addNew{
      color: #4959FF;
      font-size: 20px;
    }
  .table{
    display: grid;
    grid-template-columns: repeat(3, 4fr);
  }

  .imgPrev{
    border-radius: 24px;
    height: 88px;
  }
  .prevHead{
    display: flex;
    font-weight: bold;
  }
</style>
