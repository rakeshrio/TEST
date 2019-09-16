<template>
  <div class="home">
      <div class="fir" v-show="first">
          <div class="custom">
              <h1>First Executive Coach</h1>
        <div class="buttons">
            <button v-on:click="add('S1')">E1</button>
            <button v-on:click="add('S2')">E2</button>
        </div>
        <button class="three" v-on:click="add('S3')">E3</button>
    </div>
    <div class="custom">
        <div class="buttons">
            <button v-on:click="add('S1')">E4</button>
            <button v-on:click="add('S2')">E5</button>
        </div>
        <button class="three" v-on:click="add('S3')">E6</button>
    </div>
    <div class="custom">
        <div class="buttons">
            <button v-on:click="add('S1')" :disabled="booked">E7</button>
            <button v-on:click="add('S2')">E8</button>
        </div>
        <button class="three" v-on:click="add('S3')">E9</button>
    </div>
      </div>

    <div class="more" v-show="showmore">
        <div class="custom">
                          <h1>Second Executive Coach</h1>

        <div class="buttons">
            <button v-on:click="add('S1')">E10</button>
            <button v-on:click="add('S2')">E11</button>
        </div>
        <button class="three" v-on:click="add('S3')">E12</button>
    </div>
    <div class="custom">
        <div class="buttons">
            <button v-on:click="add('S1')">E13</button>
            <button v-on:click="add('S2')">E14</button>
        </div>
        <button class="three" v-on:click="add('S3')">E15</button>
    </div>
    <div class="custom">
        <div class="buttons">
            <button v-on:click="add('S1')">E16</button>
            <button v-on:click="add('S2')">E17</button>
        </div>
        <button class="three" v-on:click="add('S3')">E18</button>
    </div>
    </div>
    <p>{{seats}}</p>

    <button class="next" v-on:click="prev" :disabled="first">Prev</button>
    <button class="next" v-on:click="next">Next</button>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data(){
     return {
         seats:[],
         showmore:false,
         first: true,
         booked:true
     }
  },
  props: {
  },
  methods:{
      add(num){
          this.seats.push(num)
      },prev(){
          this.first = true;
            this.showmore= false;

      },
      next(){
          this.first = false;
            this.showmore= true;

      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.custom{
    background-color: red;
    width:400px;
    margin: 0px auto;
}
.buttons button{
    margin:14px 4px 4px 14px;
}
.three{
    margin-top: 10px;
}
</style>
