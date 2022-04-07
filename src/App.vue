<template>
  <div id="app">
    <h3 v-for="( name, index ) in names" :key="index"> {{ index + 1 }} {{ name }}</h3>
    <h2 v-for="( name, index ) in  fullName " :key="index">{{ index + 1 }} {{ name.first }} {{ name.last }} </h2>


  <div v-for="actor in actors" :key="actor.name">
    <h2> name: {{actor.name}}</h2>
    <p v-for="movie in actor.movies" :key="movie"> - {{ movie }}</p>
  </div>

  <h2 v-for="( value, key, index ) in myInfo" :key="value" >{{ index+1 }}. {{ key }}: {{ value }}</h2>


  <!-- conditional list rendering -->
  <div v-for="name in names" :key="name">
    <h1 v-if="name === 'bruce'">{{ name }}</h1>
  </div>
  </div>

</template>

<script>

export default {
  data(){
    return{
      names: ['bruce', 'clark', 'Vania', 'bruce', 'anasa', 'lania'],
      fullName: [
        {first: 'bruce', last: 'wayne'},
        {first: 'bruce', last: 'wayne'},
        {first: 'bruce', last: 'wayne'},
      ],
      actors:[
        {
          name:'Cristian kevin',
          movies: ['batman', 'super kaya']
        },
        {
          name:'sebastian de caprio',
          movies: ['titanic', 'inception']
        }
      ],
      myInfo:{
        name:'kavin sebastian',
        chanel:'TNT BOomm!',
        course:'Vue #3'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
