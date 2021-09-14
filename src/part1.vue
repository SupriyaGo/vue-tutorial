<template>
  <div>
    <div>Hello {{name}}</div>
    <div v-text="place"></div>
    <div v-html="dist"></div>
    <h2 v-bind:id="headingId">I am Cool!!!</h2>
    <button v-bind:disabled="isDisabled">Submit</button>
    <h2 class="underline" v-bind:class="status">Underlined text</h2>
    <h2 v-bind:class="isPromoted && 'promoted' ">Promoted</h2>
    <h2 v-bind:class="isOld ? 'old' : 'new'">Shersah</h2>
    <h2 v-bind:class="['old', 'promoted']">newly promoted movie</h2>
    <h2 v-bind:class="{
      promoted:isPromoted,
      new: !isOld,
      old: isOld
    }">Object conditional movie</h2>
    <h2 style="font-size:50px" v-bind:style="{
      color:fontColor,
      padding:'20px',
      
    }">Inline styles</h2>
    <h2 style="font-size:50px" :style="{
      color:fontColor,
      padding:'20px',

    }">Inline styles</h2>
    <h2 v-if="num === 0">The no is zero.</h2>
    <h2 v-else-if="num > 0">The no is positive.</h2>
    <h2 v-else-if="num < 0">The no is negative.</h2>
    <h2 v-else>Not a no.</h2>

    <template v-if="isDisplay">
      <h2>I am inside display condition.</h2>
    </template>

    <h2 v-show="show">Using V-Show.</h2>
    <h2 v-if="show">Using V-If.</h2>

    <h2 v-for="name in names" :key="name">{{name}}</h2>

    <template v-for="(name,index) in names" >
      <h2 :key="index">{{name}}</h2>
      <hr :key="index"/>
    </template>

    <h2 v-for="(value, key, i ) in info" :key="i">{{i + 1}}) {{key}} : {{value}} </h2>

    <h2>{{add(10,20,5)}}</h2>
    <h2>{{multiply(10)}}</h2>
  </div>
</template>

<script>

export default {
  name: 'App',
  methods:{
    add(a,b,c){
      return a+b+c;
    },
    multiply(a){
      return a * this.multiplier;
    }

    },
  data(){
    return{
      multiplier:5,
      names:['Bruce','John','Diana'],
      info:{
        name:'Supu',
        address:'Mekhliganj',
        title:'Software Engineer'
      },
      num:'a',
      isDisplay:true,
      show:true,
      name: "Supu",
      place: "Mkj",
      dist:"<b>CoochBehar</b>",
      headingId:'heading123',
      isDisabled:true,
      status:'success',
      isPromoted: true,
      isOld: true,
      fontColor:'orange'
    }
  }
}
</script>

<style>
div{
  text-align: center;
}
#heading123{
  background-color: #fafa;
  padding: 1em;
}
.underline{
  text-decoration: underline;
}
.promoted{
  font-style: italic;
}
.new{
  color: green;
}
.old{
  color: red;
}

</style>
