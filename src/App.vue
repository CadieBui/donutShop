<template>
<div id="app">
    <Header></Header>
    <router-view />
    <Footer></Footer>

</div>
</template>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    text-align: center;
    color: #2c3e50;
    background-color: #f4f1de;
}

html {
    background-color: #f4f1de;

}

#nav {

    a {
        font-weight: bold;
        color: #2c3e50;
        text-decoration: none;
        padding: 10px;
        border-radius: 10px;

        &.router-link-exact-active {
            color: white;
            background-color: #E07A5F;
        }
    }
}
</style>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
export default {

    components: {
        Header,
        Footer
    }
};
</script>
