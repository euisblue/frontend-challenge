<template>
  <div id="profile">
    <div id="header">
      
    </div>
    <img :src="getImage(name)" alt="victor">
    <div class="profile-name-age">
      <p>{{name}}</p>
      <p>{{age}}</p>
    </div>
    <div class="profile-place">
      <p>
        {{place}}
      </p>
    </div>
    <Stats :followers="followers" :likes="likes" :photos="photos"/>
  </div>
</template>

<script>
import Stats from "./Stats"

export default {
    name: "Profile",
    components: {
      Stats,
    },
    props: {
      name: String,
      age: String,
      place: String,
      followers: String,
      likes: String,
      photos: String,
    },
    methods: {
      getImage(name) {
        let [fname, lname] = name.split(' ');
        return require(`../assets/image-${fname.toLowerCase()}.jpg`);
      }
    }

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

div#header {
  position: absolute;
  background-color: red;
  background-image: url("../assets/bg-pattern-card.svg");
  width: 100%;
  height: 7em;
  z-index: -1;
}

div#profile {
  position: relative;
  width: 20em;
  height: 21em;
  text-align: center;
  border-radius: 15px;
  font-family: 'Kumbh Sans', sans-serif;
  font-weight: 400;
  margin: 10px;

  background-color: #fff;
  box-shadow: 0 0 3px 2px hsl(229, 23%, 23%);
  z-index: 0;
  overflow: hidden;

  transition: all 0.3s ease-in-out;
}

div#profile:hover {
  transform: scale(1.1);
  box-shadow: 0 0 5px 1px hsl(229, 23%, 23%);

}


div#profile img {
  margin-top: 4em;
  border: 5px solid #fff;
  border-radius: 50%;
  width: 100px;
  height: 100px;
}

div#profile .profile-name-age {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  padding: 0 10px;
}

div#profile .profile-name-age > p {
  padding: 0 4px;
}

div#profile .profile-place {
  font-size: 12px;
  margin: -15px 0 20px 0;
  color: hsl(227, 10%, 46%);
}

div#profile .profile-name-age > p:nth-child(1) {
    font-family: 'Kumbh Sans', sans-serif;
    font-weight: 700;
}

div#profile .profile-name-age > p:nth-child(2) {
    color: hsl(227, 10%, 46%);
}
</style>