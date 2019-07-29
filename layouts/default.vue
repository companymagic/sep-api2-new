<template>
  <div>
  <a href="/">home</a>&nbsp;|&nbsp;<nuxt-link to="/000">000</nuxt-link>&nbsp;|&nbsp;<nuxt-link to="/001">001</nuxt-link>&nbsp;|&nbsp;
  <div v-for="item in lp" :key="item.code">
      <nuxt-link :to="'/'+ item.code">000{{item.value}}</nuxt-link>&nbsp;|&nbsp;
    </div>
    <div>
    <a href="/007">0007</a>
    </div>
    <nuxt />
    {{this.$route.path}} | {{this.$route.params}}
  </div>
</template>
<script>
export default{
  name:"layout",
  data(){
    return{
      lp:[{code:"002",value:"2"},{code:"003",value:"3"},{code:"004",value:"4"},{code:"005",value:"5"},{code:"006",value:"6"}]
    }
  }
}
</script>
<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
