<template>
<div>
<Logo />
<button class="btn btn-primary" @click="doit">doit</button>
{{msg}}<br />
<nuxt-child />
<theBottom />
</div>
</template>

<script>
import axios from 'axios' 
import Logo from '~/components/Logo.vue'
import theBottom from '~/components/footer.vue'
export default {
  name:"category",
  data(){
    return{
    msg:"this is message"
    }
  },
  components: {
    Logo,
    theBottom
  },

  mounted: async function(){

    let s= await axios.get(`http://localhost:3001`)
    this.msg=s.data
  },
  methods:{
    doit(){
   
        this.msg = "msg changed!!"
  
    }
  }
  
}


</script>

<style>



</style>