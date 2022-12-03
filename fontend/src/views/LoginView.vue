<script>
import router from "../router";
import background from "../assets/background.png";

export default{
    data(){
        return{

        }
    },
    methods: {

    }
}
</script>

<template>
    <div class="bg"></div>
    <div class="content">
        <h1 class="title">ClassBooking</h1>
        <h2 class="subtitle">By Team2 Studio</h2>

        <router-link to="/home" class="btn btn-style-1">Se connecter</router-link>
        <router-link to="/requestaccess" class="btn btn-style-4">Demander un accès</router-link>
    </div>
</template>

<style scoped lang="scss">
    .content{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }
    .title{
        text-transform: uppercase;
        font-size: clamp(3.5rem, 2.857rem + 2.571vw, 8rem);
        color: #FFF;
    }
    .subtitle{
        position: relative;
        top: -1rem;
        font-size: clamp(1.8rem, 1.743rem + 0.229vw, 2.2rem);
        color: #eee;
        margin-bottom: 15.1rem;
    }
    .btn{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40rem;
        height: 6rem;
        font-size: 2rem;
        font-weight: 500;
        &:first-of-type{
            margin-bottom: 3.5rem;
        }
        &:hover, &:focus{
            color: #fff;
        }
    }

    @media screen and (max-width: 43.75em){
        .btn{
            display: flex;
            justify-content: center;
            align-items: center;
            width: 30rem;
            height: 4.5rem;
            font-size: 1.8rem;
            font-weight: 500;
            &:first-of-type{
                margin-bottom: 2.5rem;
            }
        }
    }
</style>