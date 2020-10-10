<template>
  <div :class="$style.container">
    <Container>
      <div :class="$style.head">
          <div :class="$style.whatever">Rent <span :class="$style.whateverBlue">whatever</span></div>
          <div :class="$style.addNew"><span>Add new</span></div>
      </div>
      <div :class="$style.tableItem">
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
                    <div :class="$style.description">{{item.description}}</div>
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
    async asyncData(){
      const items = DataItems
      return {items}
    },
    data:()=>({
        items:[]
    }),
    methods:{
      openItem(item){
       this.$router.push('/view/' + item.id)
      }
    }   
}
</script>

<style module lang='css' >
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
}
  .tableItem{
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(373px, 1fr));
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
  .prevContent{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-direction: column;
    margin-left: 32px;
  }
  .description{
    font-size: 12px;
    color: #677B8F;
  }
  .nameType::first-letter{
    text-transform: uppercase;
  }
  .rent{
    font-size: 14px;
    font-weight: bold;
    color: #F84AB3;
  }
</style>
