<template>
  <div :class="$style.container">
    <Container>
      <div :class="$style.head">
          <div :class="$style.whatever">Rent<span :class="$style.whateverBlue">whatever</span>
            <div :class="$style.arrDown">
              <svg :class="$style.svgArrDown" width="12" height="8" viewBox="0 0 12 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 8L0 1.99965L2.00094 0L6 4.00071L9.99906 0L12 1.99965L6 8Z" fill="#4959FF"/>
              </svg>
            </div>
          </div>
          <div :class="$style.addNew">
            <div>Add new</div>
            <div :class="$style.divPlus">
                <svg :class="$style.svgPlus" width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M6 6V0H8V6H14V8H8V14H6V8H0V6H6Z" fill="#FCFCFC"/>
                </svg>
            </div>
          </div>
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
    align-items: center;
    padding: 55px 0 55px 0;
    font-weight: bold;
  }
  .divPlus{
    background: #4959FF;
    width: 48px;
    height: 48px;
    border-radius: 16px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 26px;
  }
    .whatever{
      font-size: 40px;
      height: 100%;
      display: flex;
      align-items: center;
    }
      .whateverBlue{
        height: 100%;
        display: flex;
        align-items: center;
        color: #4959FF;
        margin-left: 12px;
      }
    .addNew{
      color: #4959FF;
      font-size: 20px;
      display: flex;
      align-items: center;
    }
    .arrDown{
      width: 100%;
      display: flex;
      align-items: center;
      margin-left: 24px;
    }  
  .imgPrev{
    border-radius: 24px;
    height: 88px;
  }
  .prevHead{
    display: flex;
    font-weight: bold;
    font-size: 1rem;
  }
  .prevContent{
    display: flex;
    justify-content: space-around;
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
  @media (max-width: 1100px) {
    .tableItem{
      grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
      grid-gap: 12px;
    }
    .prevContent{
      margin-left: 20px;
    }
    .whatever{
      font-size: 24px;
    }
    .head{
      padding-top:24px;
      padding-bottom:24px;
    }
    .addNew{
      font-size: 16px;
    }
    .imgPrev{
      height: 88px;
      width: auto;
      border-radius: 16px;
    }
    .divPlus{
      width: 32px;
      height: 32px;
      border-radius: 8px;
      margin-left: 12px;
    }
    .svgPlus{
      height: 11.67px;
      width: 11.67px;
    }
    .svgArrDown{
      height: 5px;
      width: 8px;
    }
    .arrDown{
      margin-left: 8px;
    } 
    .whateverBlue{
        margin-left: 6px;
    } 
    .prevHead{
      flex-wrap: wrap;
  }
  }
</style>
