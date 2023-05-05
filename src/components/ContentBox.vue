<template>

    <div>
        <ul><h3 class = "item1">  {{attractions.name}}</h3></ul>
        <ul><img class="img"  align-items=center :src="attractions.url" :alt="attractions.name"></ul>
        <ul><p class = "item"> Location : {{attractions.location}}</p></ul>
        <ul><p class = "item"> Significance : {{attractions.significance}}</p></ul>
        <ul><p class = "item"> Admission fee (USD) : ${{attractions.admissionfee}}</p></ul>
        <ul><p class = "item"> Number of Visitors   :  {{attractions.visitors}}</p></ul>
        <ul><p class = "item"> Rating : {{attractions.rating}}</p></ul>
    </div>
    

</template>

<script>


export default{
    name: 'ContentBox',
    
    props:{
        attractions: Array
    }
}


</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Italiana&family=Labrada&family=Overlock&display=swap');

h4{
    margin: 2px;
}

div{
    background-color: #dfe9eb;
    color: black;
    padding: 1em;
    align-items: center;
    
}
 
.img{
    width: 700px;
    height: 450px;
    padding: 5px;
    display: block;
    margin-left: auto;
    margin-right: auto;
    border: 0.2em solid black;
    
}

.item{
    font-size: 19px;
    min-width: 0;
    font-family: 'Labrada', serif;
    float: inline-start;
    text-align: justify;
    display: grid; 
    grid-template-columns: 1fr;
    padding: 0.5em
}
.item1{
    text-align: center;
    text-decoration: solid;
    font-family: 'Italiana', serif;
    font-size: 28px;
    color: black;
    


}






</style>