<template>
  <div class="home">

    <div class='bar'>
       <h2 class='name'>Lindokuhle's ATM</h2> 
    </div>

  <div class="text">
      <h3 class='vinote'>Welcome Lindokuhle Zwane's Atm Machine</h3>
     
    
  </div>
      <div class="container">
        <h3 class="p-3 text-center">Vue.js - Display a list of items with v-for</h3>
        <table class="table table-striped table-bordered">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Email</th>
                    <th>Role</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="user in userInfo" :key="user.id">
                    <td>{{user.account_number}} {{user.lastName}}</td>
                    <td>{{user.account_type}}</td>
                    <td>{{user.balance}}</td>
                    <td><button v-on:click="greet(user)"> withdraw</button></td>
                </tr>
            </tbody>
        </table>
    </div> 
    
  </div>
  
</template>

<style>
body{
  margin:0;
}
.bar{
  background-color: black;
  margin: 0 auto;
  width: 100%;
  height:10%;
  border-bottom: 0.5rem solid red;
}

.name{
  margin:0;
  text-align: center;
  color: white;
  font-family: 'Gamja Flower', cursive;
  padding: 0.5% 0 0 0;
  font-size: 3rem;
}

.text{
  border:0.1rem solid black;
  margin:13% auto ;
  width: 40%;
  background-color: lightgrey;
  border-radius: 1rem;
}

.vinote{
  margin:3% auto;
  text-align: center;
  font-family: 'Inconsolata', monospace;
}

.lolo{

}

#login{
  margin:0 0 0 40%;
  padding:2rem;
  border-radius:1rem;
  background-color: darkblue;
  color: white;
  width: 20%;


}

#login:hover{
   background-color: green;
}


#signup{
  margin:2% 0 2% 40%;
  padding: 2rem;
  border-radius:1rem;
  background-color: darkblue;
  color: white;
  width: 20%;
}

#signup:hover{
   background-color: green;
}





/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  body{
    background-color: red;
  }
  .text{
    width: 70%;
  }
  .vinote{
    font-size: 1.9rem;
    color:black;
  }

  #login{
    padding:0.7rem;
  }
  #signup{
    padding:0.7rem;
  }
}

@media only screen and (max-width: 408px) {
  .vinote{
    font-size: 1.5rem;
  }
  #login{
    padding:1.2% 1.2% 1.2% 1.2%;
  }
  #signup{
    padding:1.2% 1.2% 1.2% 1.2%;
  }
  .text{
    width:90%;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
    body{
    background-color: green;
  }
   
   .text{
    width: 50%;
   }
  .vinote{
    font-size: 1.9rem;
    border:0.1rem solid black;
  }

  #login{
    padding:0.7rem; 
  }

  #signup{
    padding:0.7rem;
  }
  

}



/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  body{
    background-color: blue;
  }

  .vinote{
    font-size: 2rem;
  }
  
} 

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
    body{
    background-color: purple;
  }

} 

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
    body{
   /* background-color: pink;*/
     background-color: white;
  }

}
</style>

<script>
import axios from 'axios';
import { createApp } from 'vue';
import Vue from "vue";
import VueSimpleAlert from "vue-simple-alert";

Vue.use(VueSimpleAlert);

export default {
  data: function() {
    return {
      userInfo: [],
      amount :0,
      newBalance:0,
      message: "This is the Vue_js_frontEnd - for the ATM_Machine_FrontEnd"
    };
  },
  created: function() {},
  methods: {
     greet: function (user) {
              //console.log(user.balance)
            
          this.$prompt("Enter amount").then(text => {
       this.amount = text,
        this.newBalance = user.balance - this.amount;
       console.log(this.newBalance)
     
    axios.put('http://localhost:8080/api/accounts/?account_number='+user.account_number,
          {
          'balance': JSON.stringify(user.balance)

          })
            .then((response) => {

              console.log(response.data);    
      
            })
            .catch(function(error){
              console.log(error);
            });
 
  // do somthing with text
});
  
    }
  },
   beforeMount(){

axios.get('http://localhost:8080/api/accounts#/').then(resp => {
  this.userInfo = resp.data;
  
});
   
 },
  computed: {}
};
</script>
