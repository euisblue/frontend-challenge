<template>
    <div id="panel" :style="{backgroundColor: color}">
        <img :src="getIcon(title)" :alt="title">
        <p class="title">{{ title.toUpperCase() }}</p>
        <div class="description">
        <slot name="description"></slot>
        </div>
        <Button text="Learn More" :textColor="color" />
    </div>
</template>

<script>
import Button from "../components/Button"

export default {
    name: "Panel",
    props: {
        title: String,
        icon: String,
        color: String,
    },
    methods: {
        getIcon(title) {
            return require(`../assets/icon-${title}.svg`);
        }
    },
    components: {
        Button,
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lexend+Deca&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700&display=swap');

#panel {
    padding: 40px 45px;
    max-width: 250px;
    min-width: 200px;
    color: aliceblue;
}

#panel p.title {
    font-family: 'Big Shoulders Display', cursive;
    font-weight: 700;
    font-size: 36px;
}

#panel div.description  {
    opacity: 75%;
    line-height: 25px;
    margin-bottom: 70px;
}

</style>