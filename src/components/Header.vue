<template>
    <div class="nav">
        <router-link to="/home"> Home </router-link>
        <router-link to="/add-restaurant"> Add Restaurant </router-link>
        <a v-on:click="logout" href="#"> Logout </a>
    </div>
</template>


<script>

    export default {
        name: 'HeaderComponent',
        
        methods: {
            logout() {
                localStorage.clear();
                this.$router.push({ name: 'login' });
            }
        }
    }
</script>


<style scoped>
    .nav {
        background-color: #333;
        overflow: hidden;
    }

    .nav a {
        text-decoration: none;
        float: left;
        color: #f2f2f2f2;
        padding: 16px 14px;
        text-align: center;
        font-size: 17px;
        margin-right: 5px;
    }

    .nav a:hover {
        background: #ddd;
        color: #333;
    }
</style>
