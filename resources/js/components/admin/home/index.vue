<script setup>
import { useRouter } from 'vue-router';

const router = useRouter()

const logout = () => {
    localStorage.removeItem('token')
    router.push('/')
}

</script>

<template>
    <h1>Welcome to Dashboard admin</h1>
    <div>
        <router-link to="/">Home </router-link>
    </div>
    <br>
    <button @click="logout">
        Logout
    </button>
</template>