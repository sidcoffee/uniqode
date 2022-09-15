<template>

  <div class="wrapper" :class="isAllTrue ? 'alltrue' : ''">
    <input data-index="0" ref="input-0" type="number"  @input="focusNextOncePopulated($event, 1)" :class="[isAddClassgreenone ? 'greenback' : '', isAddClassredone ? 'redback' : '', isAddClassyellowone ? 'yellowback': '', isAllTrue ? 'alltrue' : '']" v-if="allfalse" onkeypress="return (event.charCode !=8 && event.charCode ==0 || (event.charCode >= 48 && event.charCode <= 57))"  />
    <input data-index="1" ref="input-1" type="number"  @input="focusNextOncePopulated($event, 1)" :class="[isAddClassgreentwo ? 'greenback' : '', isAddClassredtwo ? 'redback' : '', isAddClassyellowtwo ? 'yellowback': '', isAllTrue ? 'alltrue' : '']" v-if="allfalse" onkeypress="return (event.charCode !=8 && event.charCode ==0 || (event.charCode >= 48 && event.charCode <= 57))" />
    <input data-index="2" ref="input-2" type="number"  @input="focusNextOncePopulated($event, 1)" :class="[isAddClassgreenthree ? 'greenback' : '', isAddClassredthree ? 'redback' : '',isAddClassyellowthree ? 'yellowback': '', isAllTrue ? 'alltrue' : '']" v-if="allfalse" onkeypress="return (event.charCode !=8 && event.charCode ==0 || (event.charCode >= 48 && event.charCode <= 57))" />
    <input data-index="3" ref="input-3" type="number"  @input="focusNextOncePopulated($event, 1)" :class="[isAddClassgreenfour ? 'greenback' : '', isAddClassredfour ? 'redback' : '',isAddClassyellowfour ? 'yellowback': '', isAllTrue ? 'alltrue' : '']" v-if="allfalse" onkeypress="return (event.charCode !=8 && event.charCode ==0 || (event.charCode >= 48 && event.charCode <= 57))" />
    <input data-index="4" ref="input-4" type="number"  @input="focusNextOncePopulated($event, 1)" maxlength="1" :class="[isAddClassgreenfive ? 'greenback' : '', isAddClassredfive ? 'redback' : '',isAddClassyellowfive ? 'yellowback': '', isAllTrue ? 'alltrue' : '']" v-if="allfalse" onkeypress="return (event.charCode !=8 && event.charCode ==0 || (event.charCode >= 48 && event.charCode <= 57))"  @keyup.enter="checkval()"/>
    <input type="button" value="Submit" class="btn" v-on:click="checkval()" v-if="seen">
<input type="button" value="Reset" class="btn-re" v-on:click="resetval()" ref="res" v-if="seen">

</div>
<div v-if="alltrue" style="padding:30px 0;">
  <img src="https://cdn.dribbble.com/users/69311/screenshots/1226327/congrats-gif-edit.gif"/>
  <h1 style="text-align:center">You have cracked the code in {{num}} try   
</h1>
<!-- <input type="text" placeholder="Enter the code to unlock your voucher" style="pointer-events: all;width:100%;font-size:22px;" ref="op"> -->
<!-- <input type="button" value="Submit" class="btn" v-on:click="openvoucher()"> -->
<!-- <div v-if="openvouchers"><img src="https://s3.amazonaws.com/thumbnails.venngage.com/template/5456834b-ba95-41a9-85b2-4abd4d313c11.png"></div> -->

</div>

</template>

<script>

    export default{
        name: "Letterbox",
        props:{
        num: String,
        numone: Number,
        numtwo: Number,
        numthree: Number,
        numfour: Number,
        numfive: Number,

         },
        data(){
          return{
            isAddClassgreenone: false,
            isAddClassredone: false,
            isAddClassyellowone: false,
            isAddClassyellowtwo: false,
            isAddClassyellowthree: false,
            isAddClassyellowfour: false,
            isAddClassyellowfive: false,
            isAddClassgreentwo: false,
            isAddClassredtwo: false,
            isAddClassgreenthree: false,
            isAddClassredthree: false,
            isAddClassgreenfour: false,
            isAddClassredfour: false,
            isAddClassgreenfive: false,
            isAddClassredfive: false,
            isAllTrue: false,
            seen:true,
            openvouchers:false,
            alltrue: false,
            allfalse: true,
            allfalsetwo:true,

          }
        },
        methods: {
    focusNextOncePopulated(event, max) {
      if (event.target.value.length === max) {
        const nextElement = this.$refs?.[
          `input-${Number(event.target.dataset.index) + 1}`
        ];
        if (nextElement) nextElement.focus();
      }
    },
    resetval(){
      const myNum = this.$refs?.[`input-${0}`]
      const myNumtwo = this.$refs?.[`input-${1}`]
      const myNumthree = this.$refs?.[`input-${2}`]
      const myNumfour = this.$refs?.[`input-${3}`]
      const myNumfive = this.$refs?.[`input-${4}`]
      myNum.value = ''
      myNumtwo.value = ''
      myNumthree.value = ''
      myNumfour.value = ''
      myNumfive.value = '';
      this.isAddClassgreenone = false
      this.isAddClassredone = false
      this.isAddClassgreentwo = false
      this.isAddClassredtwo = false
      this.isAddClassgreenthree = false
      this.isAddClassredthree = false
      this.isAddClassgreenfour = false
      this.isAddClassredfour = false
      this.isAddClassgreenfive = false
      this.isAddClassredfive = false
            

       
    },
    // openvoucher(){
    //   const open = this.$refs.op.value
    //   if(open == 28675){
    //   this.openvouchers = true}
    // },
    checkval(){
      // this.$refs.res.value = "hello"
      const n_one=this.numone
      const n_two=this.numtwo
      const n_three=this.numthree
      const n_four=this.numfour
      const n_five=this.numfive

      this.seen = false
      const myNum = this.$refs?.[`input-${0}`]
      const myNumtwo = this.$refs?.[`input-${1}`]
      const myNumthree = this.$refs?.[`input-${2}`]
      const myNumfour = this.$refs?.[`input-${3}`]
      const myNumfive = this.$refs?.[`input-${4}`]
      if(myNum.value == n_one) {
        this.isAddClassgreenone = true;

      }
      else if((myNum.value == n_two) || (myNum.value == n_three) || (myNum.value == n_four) || (myNum.value == n_five)){
        this.isAddClassyellowone = true

      }
      else{
        this.isAddClassredone = true;

      }

      if(myNumtwo.value == n_two){
        this.isAddClassgreentwo = true;
      }
      else if((myNumtwo.value == n_one) || (myNumtwo.value == n_three) || (myNumtwo.value == n_four) || (myNumtwo.value == n_five)){
        this.isAddClassyellowtwo = true

      }
      else{
        this.isAddClassredtwo = true;

      }

      if(myNumthree.value == n_three){
        this.isAddClassgreenthree = true;
      }
      else if((myNumthree.value == n_one) || (myNumthree.value == n_two) || (myNumthree.value == n_four) || (myNumthree.value == n_five)){
        this.isAddClassyellowthree = true

      }
      else{
        this.isAddClassredthree = true;

      }
      if(myNumfour.value == n_four){
        this.isAddClassgreenfour = true;
      }
      else if((myNumfour.value == n_one) || (myNumfour.value == n_two) || (myNumfour.value == n_three) || (myNumfour.value == n_five)){
        this.isAddClassyellowfour = true

      }
      else{
        this.isAddClassredfour = true;

      }
      if(myNumfive.value == n_five){
        this.isAddClassgreenfive = true;
      }
      else if((myNumfive.value == n_one) || (myNumfive.value == n_two) || (myNumfive.value == n_three) || (myNumfive.value == n_four)){
        this.isAddClassyellowfive = true
      }
      else{
        this.isAddClassredfive = true;

      }
      if((this.isAddClassgreenone == true) && (this.isAddClassgreentwo == true) &&(this.isAddClassgreenthree == true) &&(this.isAddClassgreenfour == true) &&(this.isAddClassgreenfive == true)){
        this.alltrue = true;
        // this.allfalse = false;

      }
      if(this.alltrue){
        this.isAllTrue = true;
        document.body.classList.add('nopoint')

      }
    }

  },
 

        
    }

</script>

<style scoped>
  .wrapper{display:flex;}
  .alltrue,.nopoint .wrapper{pointer-events:none!important;}
.greenback{
  background:greenyellow;
}
.redback{
  background:red
}
.yellowback{
  background: yellow;
}
input[type=number]{
    width: 50px;
    height: 50px;
    font-size: 35px;
    text-align: center;
}
@media only screen and (max-width: 600px) {
  input[type=number]{
    width: 40px;
    height: 40px;
    font-size: 20px;
    text-align: center;
}}
.secretone{
    background:lightgreen;
}
</style>