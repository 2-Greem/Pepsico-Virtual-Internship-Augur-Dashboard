<script setup>
import { ref } from 'vue';

class Distributor {
    constructor(id, name, region, LMShippedGoods, NMShippedGoods, avgMonth){
        this.id = id;
        this.name = name;
        this.region = region;
        this.LMShippedGoods = LMShippedGoods;
        this.NMShippedGoods = NMShippedGoods;
        this.avgMonth = avgMonth;
    }
}

const distributorList = ref([
    new Distributor(1002, "A Corp", "WorldWide", 100, 122, 125.6),
    new Distributor(1004, "B Corp", "Australia", 6729, 6890, 6457.6),
    new Distributor(2004, "C Corp", "Central", 5, 5, 10),
    new Distributor(5845, "U Corp", "Great Lake Region", 27681, 28762, 24825)
])
</script>

<template>
    <div>
        <!-- <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
            <h1 class="display-4">Distributors</h1>
            <p class="lead">Quickly build an effective pricing table for your potential customers with this Bootstrap example. It's built with default Bootstrap components and utilities with little customization.</p>
        </div>
        <div class="container">
            <div class="card-deck mb-3 text-center">
                <div class="card box-shadow">
                    <div class="card-header">
                        <h4 class="my-0 font-weight-normal">Distributor List</h4>
                    </div>
                    <div class="card-body">
                        <div class="table-responsive">
                            <table class="table table-striped table-sm">
                                <thead>
                                    <tr>
                                        <th>#</th>
                                        <th>Name</th>
                                        <th>Region</th>
                                        <th>Last Month Shipped Goods</th>
                                        <th>Forecasted Goods this month</th>
                                        <th>Avg goods shipped per month</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr v-for="(distributor) in distributorList" :key="distributor.id">
                                        <td>{{ distributor.id}}</td>
                                        <td>{{ distributor.name }}</td>
                                        <td>{{ distributor.region }}</td>
                                        <td>{{ distributor.LMShippedGoods }}</td>
                                        <td>{{ distributor.NMShippedGoods }}</td>
                                        <td>{{  distributor.avgMonth }}</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div> -->

    <!-- HERE -->
    
    <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom box-shadow">
        <h5 class="my-0 mr-md-auto font-weight-normal">Auger</h5>
        <!-- <nav class="my-2 my-md-0 mr-md-3">
            <a class="p-2 text-dark" href="#">Feature 1</a>
            <a class="p-2 text-dark" href="#">Feature 2</a>
            <a class="p-2 text-dark" href="#">Feature 3</a>
            <a class="p-2 text-dark" href="#">Feature 4</a>
        </nav>
        <a class="btn btn-outline-primary" href="#">Sign up</a> -->
    </div>

    <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
        <h1 class="display-4">Distributors</h1>
        <p class="lead">Quickly view the most up to date info on a range of our top distributors.</p>
    </div>

    <div class="container">
        <div class="card-deck mb-3 text-center">
            <div class="card box-shadow">
                <div class="card-header">
                    <h4 class="my-0 font-weight-normal">Distributor List</h4>
                </div>
                <div class="card-body">
                    <div class="table-responsive">
                        <table class="table table-striped table-sm">
                            <thead>
                                <tr>
                                    <th>#</th>
                                    <th>Name</th>
                                    <th>Region</th>
                                    <th>Last Month Shipped Goods</th>
                                    <th>Forecasted Goods this month</th>
                                    <th>Avg goods shipped per month</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr v-for="(distributor) in distributorList" :key="distributor.id">
                                    <td>{{ distributor.id}}</td>
                                    <td>{{ distributor.name }}</td>
                                    <td>{{ distributor.region }}</td>
                                    <td>{{ distributor.LMShippedGoods }}</td>
                                    <td>{{ distributor.NMShippedGoods }}</td>
                                    <td>{{  distributor.avgMonth }}</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>

        <footer class="pt-4 my-md-5 pt-md-5 border-top">
            <div class="row">
            <div class="col-12 col-md">
                <img class="mb-2" src="https://getbootstrap.com/docs/4.0/assets/brand/bootstrap-solid.svg" alt="" width="24" height="24">
                <small class="d-block mb-3 text-muted">© 2017-2018</small>
            </div>
            <div class="col-6 col-md">
                <h5>Features</h5>
                <ul class="list-unstyled text-small">
                <li><a class="text-muted" href="#">Cool stuff</a></li>
                <li><a class="text-muted" href="#">Random feature</a></li>
                <li><a class="text-muted" href="#">Team feature</a></li>
                <li><a class="text-muted" href="#">Stuff for developers</a></li>
                <li><a class="text-muted" href="#">Another one</a></li>
                <li><a class="text-muted" href="#">Last time</a></li>
                </ul>
            </div>
            <div class="col-6 col-md">
                <h5>Resources</h5>
                <ul class="list-unstyled text-small">
                <li><a class="text-muted" href="#">Resource</a></li>
                <li><a class="text-muted" href="#">Resource name</a></li>
                <li><a class="text-muted" href="#">Another resource</a></li>
                <li><a class="text-muted" href="#">Final resource</a></li>
                </ul>
            </div>
            <div class="col-6 col-md">
                <h5>About</h5>
                <ul class="list-unstyled text-small">
                <li><a class="text-muted" href="#">Team</a></li>
                <li><a class="text-muted" href="#">Locations</a></li>
                <li><a class="text-muted" href="#">Privacy</a></li>
                <li><a class="text-muted" href="#">Terms</a></li>
                </ul>
            </div>
            </div>
        </footer>
    </div>
</div>
</template>