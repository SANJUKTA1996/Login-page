<template>
<Header />
<div class="register">

<div class="container">  
<div class="form">
  <h1 class="heading"> Add page</h1>
<input type="text" v-model="name" placeholder="Enter Name"/>
  <input type="text" v-model="email" placeholder="Enter Mail"/>
  <input type="text" v-model="mobile" placeholder="Enter mobile number"/>
  <input type="text" v-model="address" placeholder="Enter your address"/>
  <div class="btn-container">
    
  <button class="button" v-on:click="SignUp">Add</button>
  </div>
  </div>
  </div>
  </div>
</template>
<script>
import Header from './Header.vue'
export default
{
  name: 'Add',
  components:{
    Header
  },
  mounted()
{
    let user=localStorage.getItem('user-info');
    if(!user)
    {
       this.$router.push({name:'SignUp'})   
    }
}

}
</script>
