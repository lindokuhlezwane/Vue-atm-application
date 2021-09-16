<template>
  <div class="home">
      <div class='topp'>
      </div>
     
   <router-link to='/'>
    <img src='../assets/atm_front.gif' class='monday'>
  </router-link >

  <div id='box_2'>
     <h2 class='signup'>Signup</h2>

    <!--  Firstname:  -->

     <div class='dick'>

    <div class='firstname'>
      <h3>Firstname:</h3>
     <div class='fname'>
        <input type="text" class='texty'> 
     </div>
    </div>


     <div class='lastname'>
         <h3>Lastname:</h3>
       <div class='fname'>
          <input type="text" class='texty'> 
       </div>
     </div>
     
     <div class='email'>
         <h3>Email:</h3>
       <div class='fname'>
          <input type="text" class='texty'> 
       </div>
     </div>
     
     <div class='password'>
         <h3>Password:</h3>
       <div class='fname'>
          <input type="text" class='texty'> 
       </div>
     </div>

     <div class='password_c'>
         <h3>Password_confirmation:</h3>
       <div class='fname'>
          <input type="text" class='texty'> 
       </div>
     </div>
     

     </div>

  </div>



  </div>
</template>

<style>
.topp{
  width: 100%;
  height: 4rem;
  background-color: black;
}

#box_2{
   width: 50%;
   background-color: lightgrey;
   padding: 1.3rem;
   margin:2% 0 0 27%;
   border-radius: 1rem;
}

.monday{
   width: 3%;
  margin:3% 0 0 50%;
  cursor: pointer;
}

.signup{
  text-align:center;
}

.dick{
  border:0.1rem solid black;

}

.firstname{
  border:0.1rem solid red;
  width: 30%;
  margin:0 auto;
}

.lastname{
  border:0.1rem solid red;
  width:30%;
  margin:0 auto;
}

.email{
  border:0.1rem solid red;
  width:30%;
  margin:0 auto;
}

.password{
  border:0.1rem solid red;
  width:30%;
  margin:0 auto;
}

.password_c{
  border:0.1rem solid red;
  width:30%;
  margin:0 auto;
}

.texty{
  width: 100%;
  padding:0.5rem;
  border-radius:0.5rem;
}

@media only screen and (max-width: 1188px){
  .firstname{
    width: 50%;
  }
   .lastname{
    width: 50%;
  }
   .email{
    width: 50%;
  }
   .password{
    width: 50%;
  }
  .password_c{
    width: 50%;
  }

  h2,h3{
    font-size: 2rem;
  }
}

@media only screen and (max-width: 860px){
  .firstname{
    width: 60%;
  }
   .lastname{
    width: 60%;
  }
   .email{
    width: 60%;
  }
   .password{
    width: 60%;
  }
  .password_c{
    width: 60%;
  }

   h2,h3{
    font-size: 1.6rem;
  }

}

@media only screen and (max-width: 680px){
  .firstname{
    width: 65%;
  }
   .lastname{
    width: 65%;
  }
   .email{
    width: 65%;
  }
   .password{
    width: 65%;
  }
  .password_c{
    width: 65%;
  }
}

@media only screen and (max-width: 510px){
  .firstname{
    width: 70%;
  }
   .lastname{
    width: 70%;
  }
   .email{
    width: 70%;
  }
   .password{
    width: 70%;
  }
  .password_c{
    width: 70%;
  }
}


@media only screen and (max-width: 480px){
  .firstname{
    width: 80%;
  }
   .lastname{
    width: 80%;
  }
   .email{
    width: 80%;
  }
   .password{
    width: 80%;
  }
  .password_c{
    width: 80%;
  }

  h3,h2{
    font-size: 1.5rem;
  }
}


@media only screen and (max-width: 440px){
  .firstname{
    width: 100%;
  }
   .lastname{
    width: 100%;
  }
   .email{
    width: 100%;
  }
   .password{
    width: 100%;
  }
  .password_c{
    width: 100%;
  }

  h3,h2{
    font-size: 1.5rem;
  }
}


@media only screen and (max-width: 389px){
  #box_2{
    width: 60%;
     margin:2% 0 0 20%;
     
  }
  .firstname{
    width: 100%;
  }
   .lastname{
    width: 100%;
  }
   .email{
    width: 100%;
  }
   .password{
    width: 100%;
  }
  .password_c{
    width: 100%;
  }

  h3,h2{
    font-size: 1.5rem;
  }
}

@media only screen and (max-width: 330px){
  #box_2{
    width: 70%;
     margin:2% 0 0 16%;
     
  }
  .firstname{
    width: 100%;
  }
   .lastname{
    width: 100%;
  }
   .email{
    width: 100%;
  }
   .password{
    width: 100%;
  }
  .password_c{
    width: 100%;
  }

  h3,h2{
    font-size: 1.5rem;
  }
}



</style>

<script>
export default {
  data: function() {
    return {
      message: "This is the Signup page!!"
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>
