<template>
<div class="order">
    <div class="ordercover position-relative overflow-hidden text-center">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
            <h1 class="display-4 fw-normal">Let order</h1>
            <p class="lead fw-normal pb-5">Enjoy our donut </p>
        </div>
    </div>
    <div class="container mx-auto" style="width:1000px">
        <div class="row g-5 pt-5">
            <div class="checkout col-md-5 col-lg-4">
                <h4 class="d-flex justify-content-between align-items-center mb-3">
                    <span class="text">Your cart</span>
                    <span class="badge bg-secondary rounded-pill">{{cart.length}}</span>
                </h4>
                <ul class="list-group mb-3">
                    <li class="list-group-item d-flex justify-content-between lh-sm" v-for="(products, index) in cart" :key="index">
                        <div>
                            <h6 class="productname">{{products.name}}</h6>
                        </div>
                        <span class="text-muted">{{products.cost}} NT</span>
                        <button class="deleteBtn btn btn-dark" v-on:click="removeItem(products)">Delete</button>

                    </li>
                    <li class="list-group-item d-flex justify-content-between">
                        <span>Total</span>
                        <strong>{{ value }} NT</strong>
                    </li>
                    <li class="list-group-item d-flex justify-content-between">
                        <button data-bs-toggle="modal" href="#ModalToggle" v-show="cart.length>0" id="checkout" type="button" class="btn btn-outline-dark">Check out</button>
                    </li>
                </ul>

            </div>
            <div class="product col-md-7 col-lg-8">

                <div class="menu card mb-3" style="max-width: 540px;" v-for="(products,index) in products" :key="index">
                    <div class="row g-0">
                        <div class="col-md-4">
                            <img :src="products.pic" class="productImg img-fluid" alt="">
                        </div>
                        <div class="col-md-8">
                            <div class="card-body">
                                <h5 class="card-title">{{products.name}}</h5>
                                <p class="card-text"><small class="text-muted">{{products.cost}} NT</small></p>
                                <button class="btn btn-dark" v-on:click="addItem(products)">Add to your cart</button>
                            </div>
                        </div>

                    </div>
                </div>

            </div>
        </div>
    </div>
    <div class="modal fade" id="ModalToggle" data-bs-backdrop="false" aria-hidden="true" aria-labelledby="ModalToggleLabel" tabindex="-1">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="ModalToggleLabel">Fill information</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <form>
                    <div class="modal-body">
                        <div class="mb-3">
                            <label for="Name" class="form-label">Name</label>
                            <input type="text" class="form-control" id="Name" v-model="username">
                        </div>
                        <div class="mb-3">
                            <label for="exampleInputEmail1" class="form-label">Delivery address</label>
                            <input type="text" class="form-control" id="Address" aria-describedby="Address" v-model="address">
                        </div>
                        <div class="mb-3">
                            <label for="Phone" class="form-label">Phone Number</label>
                            <input type="number" class="form-control" id="Phone" v-model="phone" aria-describedby="Phone">
                        </div>

                    </div>
                    <div class="modal-footer">
                        <button type="button" v-if="username.length==0&&phone.length==0&&address.length==0" class="btn btn-dark" data-bs-target="#Modalalert" data-bs-toggle="modal">Submit</button>
                        <button type="button" v-else class="btn btn-dark" data-bs-target="#ModalToggle2" data-bs-toggle="modal">Submit</button>

                    </div>
                </form>
            </div>
        </div>
    </div>
    <div class="modal fade" id="Modalalert" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">Alert</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">PLease fill all your information </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="ModalToggle2" data-bs-backdrop="false" aria-hidden="true" aria-labelledby="ModalToggleLabel2" tabindex="-1">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="ModalToggleLabel2">Check your product before press submit</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="mb-3 row">
                        <label for="ProductName" class="col-sm-4 col-form-label">Product Name</label>
                        <div class="col-sm-8">
                            <input type="text" v-for="(products, index) in cart" :key="index" readonly class="form-control-plaintext" id="ProductName" :value="products.name+' ( '+products.cost+' NT )'">
                        </div>
                    </div>
                    <div class="mb-3 row">
                        <label for="NameA" class="col-sm-4 col-form-label">Your Name</label>
                        <div class="col-sm-8">
                            <input type="text" readonly class="form-control-plaintext" id="NameA" :value="username">
                        </div>
                    </div>
                    <div class="mb-3 row">
                        <label for="AddressA" class="col-sm-4 col-form-label">Your Address</label>
                        <div class="col-sm-8">
                            <input type="text" readonly class="form-control-plaintext" id="AddressA" :value="address">
                        </div>
                    </div>
                    <div class="mb-3 row">
                        <label for="PhoneA" class="col-sm-4 col-form-label">Your Phone number</label>
                        <div class="col-sm-8">
                            <input type="text" readonly class="form-control-plaintext" id="PhoneA" :value="phone">
                        </div>
                    </div>
                </div>
                <div class="modal-footer">
                    <button type="button"  class="btn btn-dark" data-bs-target="#Modalsuccess" data-bs-toggle="modal">Submit</button>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="Modalsuccess" tabindex="-1" aria-labelledby="Modalsuccess" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="Modalsuccess">Order successful</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">Thank you for buying our donuts</div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" @click="()=>{this.$router.go()}" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data: function () {
        return {
            username: [],
            address: [],
            phone: [],
            products: [{
                    id: 1,
                    name: 'Chocolate Donut',
                    cost: 50,
                    pic: '/img/menudonut1.55043837.jpeg'
                },
                {
                    id: 2,
                    name: 'Chocolate Cruch Donut',
                    cost: 55,
                    pic: '/img/menudonut2.f1b7d9e2.jpeg'
                },
                {
                    id: 3,
                    name: 'Lemon Donut',
                    cost: 45,
                    pic: '/img/menudonut3.369416d1.jpeg'
                },
                {
                    id: 4,
                    name: 'Cream Donut',
                    cost: 47,
                    pic: '/img/menudonut4.64f58eb0.jpeg'
                },
                {
                    id: 5,
                    name: 'Crispy Donut',
                    cost: 50,
                    pic: '/img/menudonut5.856d9818.jpeg'
                },
                {
                    id: 6,
                    name: 'Pumpkin Donut',
                    cost: 60,
                    pic: '/img/menudonut6.7b82ba67.jpeg'
                },
                {
                    id: 7,
                    name: 'Rose Dark Chocolate Donut',
                    cost: 65,
                    pic: '/img/menudonut7.f3ccb36b.jpeg'
                },
                {
                    id: 8,
                    name: 'Vanilla Chocolate Donut',
                    cost: 49,
                    pic: '/img/menudonut8.7c6fbba0.jpeg'
                },
                {
                    id: 9,
                    name: 'Vanilla Chocolate Cruch Donut',
                    cost: 53,
                    pic: '/img/menudonut9.cb91ae0d.jpeg'
                }
            ],
            cart: [],
            value: 0

        }
    },
    methods: {
        addItem(products) {
            this.cart.push(products);
            this.value += products.cost;

        },
        removeItem(products) {
            this.cart.splice(this.cart.indexOf(products), 1);
            this.value -= products.cost;
        }
    }
}
</script>

<style lang="scss" scoped>
.order {
    margin-top: 100px;
}

label {
    float: left;
    font-weight: bold;
    color: #f19c79;
}

.btn {
    width: 50%;
    height: 20%;
}

.modal-content {
    background-color: #f5efca;

}

.modal-title {
    font-weight: bold;
    font-size: 30px;
    color: #2c3e50;
}

#checkout {
    width: 100px;
    margin: 15px auto;
}

.deleteBtn {
    font-size: 10px;
    width: 51px;
    margin: 11px 9px;
}

.menu {
    background-color: #f2cc8f;
}

.ordercover {
    background-image: url(../assets/ordercover.jpeg);
    background-size: cover;
    margin-bottom: 15px;
    padding: 100px;
    background-position: center;
    color: white;
}

.menu3,
.menu6,
.menu9 {
    background-color: #f19c79;
}

.checkout {
    width: 300px;
}

.productname {
    padding: 4px;

}

.text-muted {
    padding: 11px;
}
</style>
