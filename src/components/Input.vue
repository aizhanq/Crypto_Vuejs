<script>
export default {
    props: {
        changeAmount: {
            type: Function,
            required: true
        },
        convert: {
            type: Function,
            required: true
        }
    }
}
</script>

<template>
    <input min="0" type="number" @input="changeAmount($event.target.value)" placeholder="Enter the number"><br>
    <button @click="convert()">Convert</button>
</template>

<style scoped>
input {
    outline: none;
    width: 500px;
    position: relative;
    top: -50px;
    font-size: 1.2em;
    border-radius: 3px;
    border: 0;
    padding: 10px 15px;
    background: #fafafa;
    color: #333;
}

button {
    position: relative;
    top: -20px;
    padding: 15px 20px;
    color: #fff;
    text-transform: uppercase;
    cursor: pointer;
    border-radius: 3px;
    border: 0; 
    background: #1a032d; 
}

button :hover {
    background: #bb8d29; 
    
}
</style>