<template>
  <div class="wrapper">
     
    <p class="order"> Ordernummer: <strong> {{orderNumber}} </strong>  </p>
    <div class="drone">
      <img src="../assets/graphics/drone.svg" alt="">
    </div>
    <h1>Din beställning är på väg!</h1>
      <p class="time"> {{eta}} minuter </p>
   
   <div v-on:click="backToMenu" class="btn">
      <p class="btn-text" > OK, Cool! </p>
   </div>
  </div>
</template>

<script>


export default {
    name: 'Status',
     components:{
    
    },

    computed:{
      eta(){
       return this.$store.state.eta
      },
      orderNumber(){
        return this.$store.state.orderNumber
      }
    },
    methods:{
       backToMenu: function(){
      this.$router.push("/menu");
       this.$store.commit("resetCart");
     
    }
    }
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Work+Sans:ital,wght@0,400;0,700;1,300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=PT+Serif:wght@700&display=swap');



.wrapper {
  width: 375px;
  height: 667px;
  background: #E5674E;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  position: relative;
}

.order {
font-family: 'Work Sans', sans-serif;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 120%;
/* or 19px */

color: rgba(255, 255, 255, 0.7);

}
.time{

font-family: 'Work Sans', sans-serif;
font-style: normal;
font-weight: bold;
font-size: 22px;

color: #FFFFFF;
}
.drone{
  width: 216.29px;
height: 119.06px;

}

h1 {

font-family: 'PT Serif', serif;
font-style: normal;
font-weight: bold;
font-size: 36px;
padding: 0 48px;
color: #FFFFFF;

}

.btn {

width: 184px;
height: 55px;
display: flex;
justify-content: center;
align-items: center;
background: #FFFFFF;
border-radius: 50px;

}

.btn-text{

font-family: 'PT Serif', serif;
font-style: normal;
font-weight: bold;
font-size: 24px;
line-height: 55px;
color: #2F2926;
}
.btn:hover{
  cursor: pointer;
}

</style>