<template>
    
    <div class="Containerbox" >
        
        
        <div v-for="attractions in attractions" :key="attractions.sno" >
            
            <ContentBox :attractions="attractions"/>
            
        </div>

    </div>
    

</template>

<script>

    import ContentBox from './ContentBox.vue';


    export default{
        name: 'ContainerBox',
        components: {
    ContentBox
},
        props:{
            
            attractions: Array
        }
       
    }
    


</script>

<style scoped>

.Containerbox{


    background-color: #abc3cd;
display: grid;


}

</style>