<template>
    <div class="foo">
       <h2>{{ endLine }}</h2>
    </div>
</template>

<script>    
export default{
    name:'FooterBox',
    props:{
        endLine: String
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Italiana&family=Marcellus&family=Noto+Serif:ital@1&family=Pacifico&family=Raleway&family=Sofia&display=swap');


.foo{
    font-family: 'Pacifico', cursive;
    display: block;
    text-align: center;
    margin-top: 30px;
    background-color: #a9cccf;
    color: black;
    border: 0.1em solid black;
}
</style>