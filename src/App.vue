<script>
import Letterbox from './components/Letterbox.vue'

export default{
  name: 'App',
  data(){
          return{
   
            alltrue: false,
          }
        },
  components: {
    Letterbox,
},
methods:{


}

}

</script>
<template>
<Letterbox num='1st' :numone = '2' :numtwo = '8' :numthree = '6' :numfour = '7' :numfive = '5' />
<Letterbox num='2nd' :numone = '2' :numtwo = '8' :numthree = '6' :numfour = '7' :numfive = '5' />
<Letterbox num='3rd' :numone = '2' :numtwo = '8' :numthree = '6' :numfour = '7' :numfive = '5' />
<Letterbox num='4th' :numone = '2' :numtwo = '8' :numthree = '6' :numfour = '7' :numfive = '5'/>
<Letterbox num='5th' :numone = '2' :numtwo = '8' :numthree = '6' :numfour = '7' :numfive = '5'/>
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
  /* * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  } */
  body {
    font-family: 'Poppins', sans-serif;
  }

  .btn {
    display: inline-block;
    background: rgb(18, 201, 131);
    color: #fff;
    border: none;
    margin: 5px;
    border-radius: 5px;
    cursor: pointer;
    text-decoration: none;
    font-size: 15px;
    font-family: inherit;
  }
  .btn-re {
    display: inline-block;
    background: #f8a711ee;
    color: #fff;
    border: none;
    margin: 5px;
    border-radius: 5px;
    cursor: pointer;
    text-decoration: none;
    font-size: 15px;
    font-family: inherit;
  }
  .btn:focus {
    outline: none;
  }
  .btn:active {
    transform: scale(0.98);
  }
  .btn-block {
    display: block;
    width: 100%;
  }
  
  </style>
