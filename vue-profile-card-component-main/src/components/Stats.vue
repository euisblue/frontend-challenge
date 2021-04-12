<template>
    <div id="stats">   
        <Stat :number="followers" text="Followers" />
        <Stat :number="likes" text="Likes" />
        <Stat :number="photos" text="Photos" />
    </div>
</template>

<script> 
import Stat from "./Stat"

export default {
    name: "Stats",
    components: {
        Stat,
    },
    props: {
        followers: String,
        likes: String,
        photos: String,
    },
}
</script>

<style scoped>
div#stats {
    position: relative;
    display: flex;
    justify-content: space-evenly;
    border-top: 1px solid hsl(0, 0%, 91%);
    padding: 13px 0;
}
</style>