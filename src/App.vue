<template>
    <div>
        <app-header v-bind:title="title" @changeTitle="updateTitle($event)"></app-header>
        <app-content v-bind:gotPerson="parangaricutirimirruaru"></app-content>
        <app-footer v-bind:title="title"></app-footer>
    </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Content from './components/Examples.vue'

export default {
    components: {
        'app-header'    : Header,
        'app-footer'    : Footer,
        'app-content'   : Content
    },
    data () {
        return {
            parangaricutirimirruaru: [
                {name: 'Eddard', house: 'Stark', show: false},
                {name: 'Jamie', house: 'Lannister', show: false},
                {name: 'Robert', house: 'Baratheon', show: false},
                {name: 'Olenna', house: 'Tyrell', show: false},
                {name: 'Daenerys', house: 'Targaryen', show: false},
                {name: 'John', house: 'Snow (Aegon Targaryen)', show: false},
                {name: 'Roose', house: 'Bolton', show: false},
                {name: 'Brienne', house: 'Tarth', show: false},
                {name: 'Tyrion', house: 'Lannister', show: false},
                {name: 'Sandor', house: 'Clegane', show: false},
                {name: 'Margaery', house: 'Tyrell', show: false},
                {name: 'Theon', house: 'Greyjoy', show: false},
                {name: 'Jorah', house: 'Mormont', show: false},
                {name: 'Samwell', house: 'Tarly', show: false},
                {name: 'Myrcella', house: 'Baratheon', show: false},
                {name: 'Cercei', house: 'Lannister', show: false},
                {name: 'Gregor', house: 'Clegane', show: false},
                {name: 'Sansa', house: 'Stark', show: false},
                {name: 'Ygritte', house: 'No House / Savage', show: false},
                {name: 'Catelyn', house: 'Tully / Stark', show: false},
                {name: 'Loras', house: 'Tyrell', show: false}
            ],
            title: "What House Belongs"
        }
    },
    methods: {
        updateTitle: function(updatedTitle){
            this.title = updatedTitle;
        }
    }
}
</script>
    
<style>
body, html {
    margin: 0;
    padding: 0;
}
</style>
