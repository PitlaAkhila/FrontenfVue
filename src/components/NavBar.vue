<template>
    <div class="div1">
        <h1>{{ titleName }}</h1>
    </div>
    <div class="div2">
        <span class="line"></span>
        <span class="div2" ><h3>{{ tagLine }}</h3></span>
        <span class="line"></span>
    </div>
</template>

<script>
    export default{
        name:'NavBar',
        props:{
            titleName: String,
            tagLine: String
        }
    }

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Italiana&family=Marcellus&family=Noto+Serif:ital@1&family=Sofia&display=swap');@import url('https://fonts.googleapis.com/css2?family=Marcellus&family=Noto+Serif:ital@1&family=Playfair+Display:ital,wght@1,500&family=Sofia&display=swap');
    .div1{
        color: whitesmoke;
        font-family: 'Italiana', serif;
        text-align: center;
        font-size: 30px;
        background-color: #61828a;
        border: 0.1em solid black;
        
    }
    .div2{
        color: #050505;
        font-family: 'Italiana', serif;
        text-align: center;
        font-size: 24px;
        display: flex;
        align-items: center;
        justify-content: center;

    }
    .line {
    flex-grow: 1;
    height: 5px;
    background-color: black;
}

</style>