<template>
  <div>
    <h1>BEAUTIFUL QUOTES</h1>
    <div class="add-box">
      <input type="text" placeholder="Enter your quote here..." v-model="quote">
      <button @click="addit">ADD Quote</button>
    </div>
    <Quotes :quotes="quotes"></Quotes>
    <h1>Thanks for visiting us...</h1>
  </div>
</template>

<script>
import Quote from './quote';
export default {
  components:{
    Quotes:Quote
  },
  data:function(){
    return{
      quotes:["Good day comes after every bad day","a friend in need is a friend indeed","if u cant work according to situations then make situations work according to you."],
      quote: ''
    }
  },
  methods:{
    addit(){
      this.quotes.unshift(this.quote);
      this.quote=""
    }
  }
}
</script>

<style>
  div{
    text-align: center;
  }
  h1{
    color: darkblue;
    text-transform: uppercase;
    margin: 2rem;
  }
  .add-box{
    padding: 1rem;
    background: darkgoldenrod;
    margin: 2rem;
    display: flex;
    flex-direction: column;
    text-align: center;
    }
  button{
    width: 60px;
    margin: 1rem auto;
  }
</style>