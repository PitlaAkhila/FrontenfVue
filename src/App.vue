<template>

<!-- step3: must use the component-->
<NavBar titleName="DESTINATION AMERICA" tagLine="TOP 10 MUST VISIT ATTRACTIONS"/>
<ContainerBox   :attractions="attractions"/>
<FeaturedBox :attractions="attractions"/>
<FooterBox endLine="That's All Folks!"/>


  
</template>

<script>

//step1: import the component 
import NavBar from './components/NavBar.vue';
import ContainerBox from './components/ContainerBox.vue';
import FeaturedBox from './components/FeaturedBox.vue';
import FooterBox from './components/FooterBox.vue';


  export default{
  
    name: 'App',
    //step2:you must register the component
    components:{
      NavBar,
      ContainerBox,
      FooterBox,
      FeaturedBox,
    },
    data(){
      return{
        attractions:[]
        
      }
    },
  
    methods:{
      async fetchAttractions(){
         
          const res = await fetch('https://nodejs-t1.herokuapp.com/api') //I tried to add my name instead of "nodejs-t1" in heroku deployment but it was giving me issues which are a bit complicated
          //const res = await fetch('http://localhost:5990/api')

          const data = await res.json()
          console.log( data )
          return data
         }
         
  
    },
  
     async created(){
      this.attractions = await this.fetchAttractions()
      console.log(this.attractions)
      
    }
  }
</script>

<style>
 
body{
  margin: 5px;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

div{
  margin-bottom: 0.5em;
  padding:10px;
}


</style>