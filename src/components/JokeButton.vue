<template>
    <div>

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