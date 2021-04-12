<template>
    <div>
        <button @mouseenter="onMouseEnter" @mouseleave="onMouseLeave" :style="{'color': textColor}">{{text}}</button>
    </div>
</template>

<script> 
export default {
    name: "Button",
    props: {
        text: String,
        textColor: String,
    },
    methods: {
        onMouseEnter(e) {
            e.target.style.backgroundColor = this.textColor;
            e.target.style.boxShadow = 'none';
        },
        onMouseLeave(e) {
            e.target.style.backgroundColor = 'hsl(0, 0%, 95%)';
            e.target.style.boxShadow = '0 0 3px 1px rgba(39, 39, 39, 0.514)';

        }
    }
}
</script>

<style scoped>
button {
    position: relative;
    display: block;
    width: 125px;
    height: 40px;

    border-radius: 30px;
    outline: none;
    border: none;
    box-shadow: 0 0 3px 1px rgba(39, 39, 39, 0.514);
    
    cursor: pointer;
}

button:hover {
    border: 2px solid hsla(0, 0%, 100%, 0.75);
    color: hsla(0, 0%, 100%, 0.75) !important;
}

button:active {
    transform: scale(0.98);
}
</style>