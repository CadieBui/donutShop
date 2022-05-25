<template>
<div class="menu">
   
    <div class="commingsoon position-relative overflow-hidden text-center">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
            <h1 class="display-4 fw-normal">Menu</h1>
            <p class="lead fw-normal pb-5">New flavor will coming soon.Don't forget to comeback with us </p>
        </div>

    </div>

    <div class="container-fluid">
        <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 g-3 position-relative">
            <div class="col">
                <div v-on:mouseover="upHere=true" v-on:mouseleave="upHere=false" class="card shadow-sm ">
                    <img src="../assets/menudonut1.jpeg" class="img" alt="">
                    <div class="card-img-overlay shadow-lg" v-if="upHere">
                        <p class="card-text">Chocolate Donut</p>
                        <div class="btn">
                            <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere1=true" v-on:mouseleave="upHere1=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut2.jpeg" class="" alt="">
                    <div class="card-img-overlay shadow-lg" v-if="upHere1">
                        <p class="card-text">Chocolate Cruch Donut</p>
                        <div class="btn ">
                            <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere2=true" v-on:mouseleave="upHere2=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut3.jpeg" class="" alt="">
                    <div class="card-img-overlay shadow-lg " v-if="upHere2">
                        <p class="card-text">Lemon Donut</p>
                        <div class="btn">
                            <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col">
                <div v-on:mouseover="upHere3=true" v-on:mouseleave="upHere3=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut4.jpeg" class="" alt="">
                    <div class="card-img-overlay shadow-lg" v-if="upHere3">
                        <p class="card-text">Cream Donut</p>
                        <div class="btn">
                            <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere4=true" v-on:mouseleave="upHere4=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut5.jpeg" class="" alt="">
                    <div class="card-img-overlay shadow-lg " v-if="upHere4">
                        <p class="card-text">Crispy Donut</p>
                            <div class="btn">
                                <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                                </router-link>
                            </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere5=true" v-on:mouseleave="upHere5=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut6.jpeg" class="" alt="">

                    <div class="card-img-overlay shadow-lg " v-if="upHere5">
                        <p class="card-text">Pumpkin Donut</p>
                            <div class="btn-group">
                                <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                                </router-link>
                            </div>
                    </div>
                </div>
            </div>

            <div class="col">
                <div v-on:mouseover="upHere6=true" v-on:mouseleave="upHere6=false" class="card shadow-sm hoverable ">

                    <img src="../assets/menudonut7.jpeg" class="" alt="">

                    <div class="card-img-overlay shadow-lg " v-if="upHere6">
                        <p class="card-text">Rose Dark Chocolate Donut</p>
                            <div class="btn-group">
                                <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                                </router-link>
                            </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere7=true" v-on:mouseleave="upHere7=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut8.jpeg" class="" alt="">

                    <div class="card-img-overlay shadow-lg" v-if="upHere7">
                        <p class="card-text">Vanilla Chocolate Donut</p>
                            <div class="btn-group">
                                <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                                </router-link>
                            </div>
                    </div>
                </div>
            </div>
            <div class="col">
                <div v-on:mouseover="upHere8=true" v-on:mouseleave="upHere8=false" class="card shadow-sm hoverable ">
                    <img src="../assets/menudonut9.jpeg" class="" alt="">

                    <div class="card-img-overlay shadow-lg " v-if="upHere8">
                        <p class="card-text">Vanilla Chocolate Cruch Donut</p>
                            <div class="btn-group">
                                <router-link :to="{ name: 'Order' }"> <button type="button" class="btn btn-sm btn-outline-dark">Order now</button>
                                </router-link>
                            </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
</div>
</template>

<style scoped>
.menu
{
  margin-top: 100px;
}

.commingsoon {
    background-image: url(../assets/commingsoon.jpeg);
    background-size: cover;
    margin-bottom: 15px;
    padding: 100px;
}

.card-img-overlay {
    color: black;
    background-color: rgba(255, 235, 205, 0.529);
}

.card:hover {
    transform: scale(1.05);
    box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);

}

.card-text {
    text-align: center;
    /* bottom: 0;
    position: absolute;
    right: 0; */

}
</style>

<script>
export default {

    data: function () {
        return {
            upHere: false,
            upHere1: false,
            upHere2: false,
            upHere3: false,
            upHere4: false,
            upHere5: false,
            upHere6: false,
            upHere7: false,
            upHere8: false

        }
    }

};
</script>
