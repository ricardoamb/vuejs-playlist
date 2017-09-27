<template>
    <div id="characters">
        <ul>
            <li v-for="char in gotPerson" @click="char.show = !char.show">
                <h2>{{ char.name }}</h2>
                <h3 v-show="char.show">House: {{ char.house }}</h3>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        gotPerson: {
            type: Array,
            required: true
        }
    },
    data () {
        return {
            
        }
    },
    methods: {

    } 
}
</script>
    
<style scoped>

    #characters {
        width: 100%;
        max-width: 1200px;
        margin: 40px auto;
        padding: 0 20px;
        box-sizing: border-box;
        font-family: sans-serif;
        font-weight: 100;
    }
    ul {
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        padding: 0;
    }
    li {
        flex-grow: 1;
        flex-basis: 300px;
        text-align: center;
        padding: 30px;
        border: 1px solid #333;
        margin: 10px;
        cursor: pointer;
    }
    li h3{
        background: #333;
        color: #FFF;
        padding: 10px 0;
        font-weight: bold;
    }

</style>
