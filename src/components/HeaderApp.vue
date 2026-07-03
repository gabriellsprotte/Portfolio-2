<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <header class="fixed-header">
        <nav>
            <ul class="nav-menu">
                <li><RouterLink to="/">Home</RouterLink></li>
                <li><RouterLink to="/about">About</RouterLink> </li>
                <li><RouterLink to="/projects">Projects</RouterLink></li>
                <li><RouterLink to="/connect">Connect</RouterLink></li>
            </ul>
        </nav>
    </header>
</template>

<style scoped>
    .fixed-header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 24px 0;
    z-index: 1000;
}

.nav-menu {
    display: flex;
    background-color: #ffffff;
    padding: 10px 4px;
    border: #c0c0c0 solid 1px;
    border-radius: 30px;
    list-style: none;
    gap: 6px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.04);
}

.nav-menu a {
    text-decoration: none;
    color: #666666;
    padding: 10px 24px;
    border-radius: 20px;
    font-size: 14px;
    font-weight: 500;
    transition: all 0.25s ease;
}

.nav-menu a:hover {
    background-color: #111111;
    color: #ffffff;
}

.scroll-container {
    display: flex;
    width: 400vw;
    height: 100vh;
    overflow-x: auto;
    overflow-y: hidden;
    scroll-snap-type: x mandatory;
}

.page-section {
    width: 100vw;
    height: 100vh;
    scroll-snap-align: start;
    flex-shrink: 0;
    padding-top: 120px;
    overflow-y: auto; 
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 24px 80px 24px;
}

.split-hero-container {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 225px;
    margin-bottom: 48px;
    width: 100%;
}

.split-hero-container h1 {
    font-size: 48px;
    font-weight: 700;
    color: #000000;
    flex: 1;
    min-width: 250px;
}

.split-hero-container p {
    font-size: 20px;
    color: #666666;
    line-height: 1.6;
    flex: 1.5;
}

.split-hero-container strong {
    color: #111111;
    font-weight: 600;
}
</style>
