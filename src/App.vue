<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <h1>{{site}}</h1>
    <p v-if="ok">这是一个测试</p>
    <p v-else>不显示</p>
    <p v-if="type == 'c'">A</p>
    <h1 v-show="seen">hello</h1>
    <ol>
    <li v-for="site in sites" :key="site.name">
      {{ site.name }}
    </li>
    </ol>
    <ul>
      <li v-for="value in object" :key="value">
      {{ value }}
      </li>
    </ul>
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  data () {
    return {
      site: 'test',
      seen: true,
      ok: false,
      type: 'c',
      sites: [
        {name: 'roob'},
        {name: 'google'}
      ],
      object: {
        name: 'cainiao',
        url: 'http',
        slogan: 'jishu'
      }
    }
  },
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
