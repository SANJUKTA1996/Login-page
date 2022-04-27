<template>
<Header />

<div class="register">

<div class="container">  
<div class="form">
  <h1 class="heading"> Update Page</h1>
<input type="text" v-model="name" placeholder="Enter Name"/>
  <input type="text" v-model="email" placeholder="Enter Mail"/>
  <input type="password" v-model="password" placeholder="Enter Update Password"/>
  <input type="password" v-model="repass" placeholder="ReEnter Password"/>
  <div class="btn-container">
    
  <button class="button" v-on:click="SignUp">Update</button>
  </div>
  </div>
  </div>
  </div>

</template>
<script>
import Header from './Header.vue'
export default
{
  name: 'Update',
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
