<template>
  <div id="content">
    <ProfileCard name="Victor Crest" age="22" place="London" followers="80k" likes="803k" photos="1.4k"/>
    <ProfileCard name="Eu Bug" age="19" place="Japan" followers="92" likes="123" photos="1"/>
  </div>
    <!-- <Attribution name="imeubug"/> -->
</template>

<script>

import ProfileCard from "./components/ProfileCard";
import Attribution from "./components/Attribution";

export default {
  name: 'App',
  components: {
    ProfileCard,
    Attribution,
  }
}
</script>

<style>
div#content {
  display: flex;
  justify-content: center;
  margin: 0 auto;
  padding-top: 12em;
  height: 600px;
  background-color: hsl(185, 75%, 39%);
  background-image: url(./assets/bg-pattern-top.svg), url(./assets/bg-pattern-bottom.svg);;
  background-position: -500px -500px, 800px 500px;
  background-repeat: no-repeat, no-repeat;
}
</style>
