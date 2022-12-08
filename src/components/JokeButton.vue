<template>
    <div>
        <button>Press for Loud Joke</button>
        <button>Press for Snake Joke</button>
        <button @click="response">Press for Normal Joke</button>
    </div>
</template>

<script>
import axios from "axios";

    export default {
        name : "JokeButton",


        mounted () {
            axios.request ({
                url : "https://geek-jokes.sameerkumar.website/api?format=json",
                method : "get"
            }).then((response)=> {
                console.log(response.data.data);
            }).catch((error) => {
                console.log(error);
            })
        }
    }
   
</script>

<style scoped>

</style>