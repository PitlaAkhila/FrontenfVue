<template>
    <div class="featuredcontent">
    <span class="line"></span>
    <span class="text">Featured</span>
    <span class="line"></span>
    </div>
    <div class="box">
        <p>In this featured content we have curated a list of top destinations categorized into three unique categories.Whether you're seeking outdoor thrills, family fun, or exciting nightlife, we've got you covered. Explore your options by clicking on the links below!</p>
    <div class="places" @click="showDetails1=!showDetails1">
        <p>Family-Friendly Destinations</p>
    </div>
    <div v-if="showDetails1" class="details">
    <ul><h3>Walt Disney World:</h3> This theme park offers endless entertainment for all ages, with attractions, shows, and characters beloved by families.</ul>
    <ul><h3>National Mall:</h3> The National Mall is home to some of the most iconic monuments and museums in the United States, making it an ideal destination for families who want to explore the history and culture of the country together.</ul>
    <ul><h3>Niagara Falls:</h3> This natural wonder is a breathtaking sight for all ages, with plenty of opportunities for families to take in the scenery and enjoy activities such as boat rides and walking tours.</ul>
    </div>
    <div class="places" @click="showDetails2=!showDetails2">
        <p>Nightlife hotspots</p>
    </div>
    <div v-if="showDetails2" class="details">
    <ul><h3>French Quarter:</h3> This historic district in New Orleans is famous for its lively nightlife, music scene, and party atmosphere.</ul>
    <ul><h3>Universal Studios:</h3> This theme park offers a range of entertainment options, from rides and shows to restaurants and nightlife.</ul>
    <ul><h3>Mount Rushmore:</h3> While not traditionally thought of as a party destination, Mount Rushmore hosts a range of events throughout the year, including concerts and festivals, making it a great place to celebrate with friends and family.</ul>
    </div>
    <div class="places" @click="showDetails3=!showDetails3">
        <p>Outdoor adventure spots</p>
    </div>
    <div v-if="showDetails3" class="details">
    <ul><h3>Grand Canyon:</h3> With its stunning vistas and hiking trails, the Grand Canyon is an adventure seeker's paradise.</ul>
    <ul><h3>Yellowstone National Park:</h3> This park offers a range of outdoor activities, from hiking and camping to wildlife watching and geothermal exploration.</ul>
    <ul><h3>Golden Gate Bridge:</h3> For those who love heights and spectacular views, the Golden Gate Bridge is a must-visit.</ul>
    </div>
</div>
</template>

<script>
    export default{
        name:'FeatureBox',
        props:{
        attractions: Array
    },
    data(){
        return{
            showDetails1:false,
            showDetails2:false,
            showDetails3:false,

        }

    }

    }
    
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Italiana&family=Marcellus&family=Noto+Serif:ital@1&family=Pacifico&family=Raleway&family=Sofia&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Italiana&family=Labrada&display=swap');

.featuredcontent{
    color: #050505;
    margin-top: 5px;
    font-family: 'Pacifico', cursive;
    text-align: center;
    font-size: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.line {
    flex-grow: 1;
    height: 5px;
    background-color: black;
    margin: 0%;
}

.text {
    margin: 0 10px;
}
.box{
    background-color: #abc3cd;
    color: black;
    font-family: 'Labrada', serif;
    font-size: 19px;
    
}
.places{
    background-color: #dfe9eb;
    font-family: 'Labrada', serif;
    margin-top: 2%;
    text-align: left;
    
}
.places :hover {
    background-color: whitesmoke;
    color: black;
  }
.details{
    background-color: #a9cccf;
    font-family: 'Labrada', serif;
    margin-top: 2%;
}

</style>