<template>
    <img class="logo" src="../assets/logo.png">
    <h1>Sign Up</h1>
    <div class="register">
        <input type="text" v-model="name" placeholder="Enter Name" />
        <input type="text" v-model="email" placeholder="Enter Email" />
        <input type="password" v-model="password" placeholder="Enter Password" />
        <button v-on:click="signUp" >Sign Up</button>
    </div>

</template>

<script>
import axios from 'axios'
export default {
    name: 'SignUp',
    data()
    {
        return {
            name:'',
            email:'',
            password:''
        }
    },
    methods:{
        async signUp()
        {
           let result = await axios.post("http://localhost:3000/users", {
                email:this.email,
                password:this.password,
                name:this.name
           });
           
           console.log(result);
           if(result.status==201)
           {
            alert("sign up done");
            localStorage.setItem("user-info",JSON.stringify(result.data))
           }
        }
    }
}


</script>

<style>
.logo {
  height: 100px;
}
.register input {
    width: 300px;
    height: 40px;
    padding-left: 20px;
    display: block;
    margin-bottom: 30px;
    margin-right: auto;
    margin-left: auto;
    border: 1px solid blue;
}

.register button {
    width: 200px;
    height: 40px;
    border-radius: 10px;
    font-size: 20px;
    background-color: skyblue;
    cursor: pointer;
}
</style>

