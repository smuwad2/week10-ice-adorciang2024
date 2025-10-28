<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        props: {
            subject: String, 
            entry: String,
            mood: String
        },
        computed: {
            imgLocation() {
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here Use boostrap card --> 
    <div class="card" style="width: 18rem;">
        <img :src="imgLocation" class="card-img-top"></img>
        <div class="card-body">
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}<br></br></p>
            <slot></slot>
        </div>
    </div>
</template>

