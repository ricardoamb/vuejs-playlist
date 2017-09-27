<template>
    <header>
        <h1 @click="changeTitle">{{ title }}</h1>
    </header>
</template>

<script>
import {bus} from '../main';

export default {
    props: {
        title: {
            type: String
        }
    },
    data () {
        return {
           
        }
    },
    methods: {
        changeTitle: function(){
            //this.$emit('changeTitle','Vue Wizards');
            this.title = 'Vue Wizards';
            bus.$emit('titleChanged','Vue Wizards');
        }
    }
}
</script>
    
<style scoped>
header {
    background: lightgreen;
    padding: 10px;
}
h1 {
    color: #333;
    text-align: center;
    font-family: sans-serif;
    font-weight: 100;
}
</style>
