<template>
<div class="about">
    <div class="aboutus position-relative overflow-hidden text-center">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
            <h1 class="display-4 fw-normal">About me</h1>
            <p class="lead fw-normal pb-5">Hope our customer will like my website</p>
        </div>

    </div>
    <div class="container">
        <div class="row featurette" style="padding: 53px 0px;">
            <div class="introduction col-sm-5">
                <ol class="list-group">
                    <li class="list-group-item list-group-item-warning">
                        <h5>Bui Thi Quynh Nhu ( 裴氏瓊如 ) </h5>
                    </li>
                    <li class="list-group-item list-group-item-warning">
                        <h5>Vietnamese</h5>
                    </li>
                    <li class="list-group-item list-group-item-warning">
                        <h5>Web Designer: </h5>
                        Front-end & Back-end
                    </li>
                    <li class="list-group-item list-group-item-warning">
                        <h5>Yuanze University</h5> Information Communication
                    </li>
                    <li class="list-group-item list-group-item-warning">
                        <h5>Website design tool</h5> Vue.js, boostrap template
                    </li>
                </ol>
            </div>
            <!-- <div class="vr p-0 mx-1"></div> -->
            <div class="col-sm-5">
                <img src="../assets/aboutme.jpeg" class="pic" alt="" width="400px" height="400px">
            </div>
        </div>
    </div>
</div>
</template>

<style scoped>
.about {
    margin-top: 100px;
}

.container {
    background-image: linear-gradient(#f9c6c9, #faedcb, #dbcdf0);
}

.pic {
    margin-top: 100px;
    position: relative;
}

h4 {
    position: absolute;
}

.aboutus {
    background-image: url(../assets/aboutus.jpeg);
    background-size: cover;
    margin-bottom: 15px;
    padding: 100px;
    background-position: center;
}

.introduction {
    margin-top: 100px;
    color: #6d703f;
    font-family: Luminari, fantasy;
    text-align: start;
    width: 54%;

}

ul {
    text-decoration: none;
}

li {
    padding: 17px 33px;
    margin: 12px 21px;
    text-align: center;
}

h5 {
    font-weight: bold;

}
</style>
