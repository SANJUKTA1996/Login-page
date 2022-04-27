<template> 
<div class="container">  
<div class="form">  
                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
<h1 class="text"> Sign Up</h1>
                                                                                                                                                  

<div class="register">
  <input type="text" v-model="name" placeholder="Enter Name"/>
  <input type="text" v-model="email" placeholder="Enter Mail"/>
  <input type="password" v-model="password" placeholder="Enter Password"/>
  <div class="btn-container">
    
  <button class="button" v-on:click="SignUp">Sign Up</button>
  
  <p>
    <router-link to="/login"  class="link-style">Login</router-link>
    </p>
    
  </div>
  </div>
  </div>
  </div>
</template>

<script>
import axios from 'axios'
export default{
    name:'SignUp',
    data()
    {
        return{
            name:'',
            email:'',
            password:''
        }
    },
    methods:{
       async  SignUp()
        {
            console.warn("SignUp",this.name,this.email,this.password)
         let result=await axios.post("http://localhost:3000/users",{
             email:this.email,
             password:this.password,
             name:this.name
         });
         console.warn(result);
         if(result.status==201)
         {
             localStorage.setItem("user-info",JSON.stringify(result.data))
             this.$router.push({name:'Home'})
         }
        }
    },
mounted()
{
    let user=localStorage.getItem('user-info');
    if(user)
    {
       this.$router.push({name:'Home'})   
    }
}
  
} 

</script>

<style>

</style>
