<template>
<div>
    <div id="nav">
        <nav class="navbar navbar-expand-sm">
            <div class="container">
                <a class="navbar-brand" href="#"><img style=" width: 80px;height: 70px;" src="../assets/donut.png" alt=""></a>
                <div class="navbar-collapse ms-sm-5" id="navbarSupportedContent">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <a class="nav-link active" aria-current="page" href="#">
                                <router-link to="/">Home</router-link>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">
                                <router-link :to="{ name: 'About' }">About</router-link>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link">
                                <router-link :to="{ name: 'Menu' }">Menu</router-link>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link">
                                <router-link :to="{ name: 'Order' }">Order</router-link>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

#nav {
    position: fixed;
    /* fixing the position takes it out of html flow - knows
                   nothing about where to locate itself except by browser
                   coordinates */
    left: 0;
    /* top left corner should start at leftmost spot */
    top: 0;
    /* top left corner should start at topmost spot */
    width: 100vw;
    /* take up the full browser width */
    z-index: 200;
    /* high z index so other content scrolls underneath */
    height: 100px;
    /* define height for content */
    background-color: #c9cba3;
}
.container
{
        background-color: #c9cba3;

}
</style>
