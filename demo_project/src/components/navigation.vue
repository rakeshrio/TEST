<template>
  <div class="hello">
      <button v-on:click="toggler = !toggler">Toggler</button>
    <div class="navigation" v-show="toggler">
        <ul>
            <li><a href="#"></a>Home</li>
                        <li><a href="#"></a>About</li>
            <li><a href="#"></a>Gallery</li>
            <li><a href="#"></a>About</li>

        </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
      return{
          toggler:false
      }
  },
  props: {
  },
  methods:{

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
.navigation ul{
    text-decoration:none;
    display:inline-block;
}
.navigation ul{
    text-decoration:none;
    display:inline-block;
}
<style scoped>
</style>
