<template>
  <div>
<!--    <div class="demo" @click="attached =!attached"></div>-->
<!--    <div class="demo" :class="{red:attached, blue: !attached}"></div>-->
<!--    <div class="demo" :class="color"></div>-->
<!--    <div class="demo" :style="{backgroundColor:color}"></div>-->
<!--    <div class="demo" :style="myClasses"></div>-->
<!--    <input type="text" v-model="color">-->
<!--    <input type="text" v-model="width">-->
<!--    <div v-if="show">-->
<!--      <p> you can see me</p>-->
<!--    </div>-->
<!--    <div v-else>-->
<!--      <p>Now you can see mee!</p>-->
<!--    </div>-->
<!--    <button @click="show = !show">switch text</button>-->
<!--  -->
    <ul>
      <li v-for="(ingridient, i) in ingridients" :key="i">
        {{ingridient}}
      </li>
    </ul>

<ul>
  <li v-for="(person, index) in persons" :key="index">
    <div v-for="(value, key, i) in person" :key="i">
      {{value}}-{{key}}
    </div>
  </li>
</ul>




  </div>



</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      title: 'history of smb:',
      nameGirl: 'Lida',
      nameBoy: 'Dima',
      attached: false,
      color:'green',
      width: 100,
      show:false,
      ingridients:['meat', 'fruit', 'cookies'],
      persons:[
        {name:'Jake', age:29, color: 'black'},
        {name:'Kook', age:28, color: 'red'}
        ]
    }
  },
  computed:{
    divClasses(){
      return{
        red: this.attached,
        blue: !this.attached
      }
    },
    myClasses(){
      return{
        backgroundColor: this.color,
        width: this.width +'px'
      }
    }
  },

  methods:{
    sayHello(){
      return this.title = 'its true?'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.demo{
  width: 100px;
  height: 100px;
  background-color: gray;
  display: inline-block;
  margin: 10px;

}
.red{
  background-color: red;
}
.yellow{
  background-color: yellow;
}
.blue{
  background-color: blue;
}

</style>
