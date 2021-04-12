<template>
    <div id="stat">
        <p class="stat-number">{{number}}</p>
        <p class="stat-desc">{{text}}</p>
    </div>
</template>

<script> 
export default {
    name: "Stat",
    props: {
        number: String,
        text: String,
    }
}
</script> 

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

p {
    margin: 5px 0;
}

div#stat {
    text-align: center;
    padding: 10px 25px;
}

div#stat p.stat-number {
    font-family: 'Kumbh Sans', sans-serif;
    font-weight: 700;
    font-size: 18px;
}

div#stat p.stat-desc {
    font-size: 10px;
    color: hsl(0, 0%, 59%);
    letter-spacing: 1px;
    margin: 0;
}

</style>