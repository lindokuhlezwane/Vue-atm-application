<template>
  <div class="home">
    <div class='top'>
    </div>


    <router-link to='/'>
    <img src='../assets/atm_front.gif' class='mon'>
  </router-link >

     <div id='box_1'>
       <h2 class='logs'>Login</h2>

      <!--Email: -->
       <div class='mail'>
          <div class='em'>Email:</div> 
         <input type="email" class='mailbox'style="padding: 1%;">
       </div>

  <!--Password:-->

      <div class='pass'>
         <div class='pa'>Password:</div>
         <input type="password" class='password_box'>

      </div>

     </div> 



  </div>
</template>

<style>
.top{
  width: 100%;
  height: 4rem;
  background-color: black;
}

.mon{
  width: 3%;
  margin:3% 0 0 50%;
  cursor: pointer;
}

#box_1{
  width: 50%;
  margin:4% 0 0 27% ;
  background-color: lightgrey;
  height: 25rem;
  padding: 1.3rem;
  border-radius: 1rem;

}

.mail{
/*  border:0.1rem solid black;
*/  width: 30%;
  margin:0 auto;
}

.pass{
  width: 30%;
  /*border:0.1rem solid black;
*/  margin:0 auto;
}

.logs{
  text-align:center;
}

.em{
  font-size: 2rem;
}

.pa{
  font-size: 2rem;
}

.mailbox{
  width: 100%;
  border-radius: 0.1rem;
}

.password_box{
  padding:1%;
  width: 100%;
  border-radius:0.1rem;
}

@media only screen and (max-width: 784px) {
     .logs{
        font-size: 2rem;
     }
      .em{
        font-size: 1.4rem;
      }
      .pa{
        font-size: 1.4rem;
      }


  }

  @media only screen and (max-width: 572px) {
     .logs{
        font-size: 1.7rem;
     }

     .em{
      font-size: 1.3rem;
     }

     .pa{
      font-size: 1.3rem;
     }

  }

    @media only screen and (max-width: 352px) {
     .logs{
        font-size: 1.4rem;
     }

     .em{
       font-size: 1rem;
     }

     .pa{
      font-size: 1rem;
     }

  }

  @media only screen and (max-width: 980px){
    .mail{
      border:0.1rem solid black;
      width: 45%;
    }
    .pass{
       border:0.1rem solid black;
       width: 45%;
    }
  }

   @media only screen and (max-width: 497px){
    .mail{
      border:0.1rem solid black;
      width: 65%;
    }
    .pass{
       border:0.1rem solid black;
       width: 65%;
    }
  }

     @media only screen and (max-width: 346px){
    .mail{
      border:0.1rem solid black;
      width: 75%;
    }
    .pass{
       border:0.1rem solid black;
       width: 75%;
    }
  }





</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to the Login Page"
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>
