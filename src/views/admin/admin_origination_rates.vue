<template>
<div id="rates">
<div class="wrapper">
            <header class="topnavbar-wrapper">
    <!-- START Top Navbar-->
    <nav role="navigation" class="navbar topnavbar">
        <!-- START navbar header-->
        <div class="navbar-header">
            <a href="/" class="navbar-brand">
                <div class="brand-logo">
                    <img src="http://portal.opentact.org/img/logo.png" alt="App Logo" class="img-responsive">
                </div>
                <div class="brand-logo-collapsed">
                    <img src="http://portal.opentact.org/img/logo-single.png" alt="App Logo" class="img-responsive">
                </div>
            </a>
        </div>
        <!-- END navbar header-->
        <!-- START Nav wrapper-->
        <div class="nav-wrapper">
            <!-- START Left navbar-->
            <ul class="nav navbar-nav">
                <li>
                    <!-- Button used to collapse the left sidebar. Only visible on tablet and desktops-->
                    <a href="#" data-toggle-state="aside-collapsed" class="hidden-xs" title="Collapse/expand sidebar">
                        <em class="fa fa-navicon"></em>
                    </a>
                    <!-- Button to show/hide the sidebar on mobile. Visible on mobile only.-->
                    <a href="#" data-toggle-state="aside-toggled" data-no-persist="true" class="visible-xs sidebar-toggle">
                        <em class="fa fa-navicon"></em>
                    </a>
                </li>
                <!-- START User avatar toggle-->
                <li>
                    <!-- Button used to collapse the left sidebar. Only visible on tablet and desktops-->
                    <a id="user-block-toggle" href="#user-block" data-toggle="collapse" title="Show/hide user block">
                        <em class="icon-user"></em>
                    </a>
                </li>
                <!-- END User avatar toggle-->
                <!-- START lock screen-->
                <li>
                    <a v-on:click="logout()" class="ceil_bar_hover" title="Log out">
                        <em class="icon-logout"></em>
                    </a>
                </li>
                <!-- END lock screen-->
            </ul>
                    </div>
    </nav>
    <!-- END Top Navbar-->
</header>            <aside class="aside">
    <!-- START Sidebar (left)-->
    <div class="aside-inner">
        <nav data-sidebar-anyclick-close="" class="sidebar">
            <!-- START sidebar nav-->
            <ul class="nav">
                <!-- START user info-->
                <li class="has-user-block">
    <div id="user-block" class="collapse">
        <div class="item user-block">
            <!-- User picture-->
            <div class="user-block-picture">
                <a href="http://portal.opentact.org/edit-profile/15" data-target="#myModal" data-toggle="modal">
                    <div class="user-block-status">
                            <img src="http://portal.opentact.org/img/user/userpic.png" alt="Avatar" title="Click to edit" width="60" height="60" class="img-thumbnail img-circle">
                            <div class="circle circle-success circle-lg"></div>
                    </div>
                </a>
            </div>
            <!-- Name and Job-->
            <div class="user-block-info">
                <span class="user-block-name">Hello, Admin</span>
                    <span class="user-block-role">
                                                    Administrator
                                                                    </span>
            </div>
        </div>
    </div>
</li>                <!-- END user info-->
                <!-- Iterates over all sidebar items-->
                <li class="nav-heading ">
                    <span data-localize="sidebar.heading.MORE">Settings</span>
                </li>
                <!--<li class=" ">
                    <a href="#emails" title="Email configuration" data-toggle="collapse">
                        <em class="icon-envelope-open"></em>
                        <span>E-mail requests</span>
                    </a>
                    <ul id="emails" class="nav sidebar-subnav collapse">
                        <li class=" ">
                            <router-link to="/authorization" title="Modify authorization e-mail">
                                <span>Authorization e-mail</span>
                            </router-link>
                        </li>
                        <li class=" ">
                            <router-link to="/e_mail_confirm" title="Modify confirmation e-mail">
                                <span>Confirmation e-mail</span>
                            </router-link>
                        </li>
                    </ul>
                </li>
                <li class=" ">
                    <router-link to="/system">
                                <em class="icon-docs"></em>
                                <span>System logs</span>
                    </router-link>
                </li>
                <li class=" ">
                    <router-link to="/admin">
                                <em class="icon-users"></em>
                                <span>Modification log</span>
                    </router-link>
                </li>-->
                <li class=" ">
                    <router-link to="/dev">
                            <em class="icon-users"></em>
                            <span>Developers</span>
                    </router-link>
                </li>
                <li class=" ">
                    <router-link to="/did_ven">
                            <em class="icon-users"></em>
                            <span>Did Vendors</span>
                    </router-link>
                </li>
                <li class=" ">
                    <a href="#costs" title="Manage costs" data-toggle="collapse">
                        <em class="fa fa-money"></em>
                        <span>Costs</span>
                    </a>
                    <ul id="costs" class="nav sidebar-subnav collapse">
                        <li class=" ">
                            <router-link to="/cost_did">
                                        <em class="icon-users"></em>
                                        <span>DID Cost</span>
                            </router-link>
                        </li>
                        <li class=" ">
                            <router-link to="/cost_sms">
                                            <em class="icon-users"></em>
                                            <span>SMS Cost</span>
                            </router-link>
                        </li>
                    </ul>
                </li>
               <li class=" ">
                            <a href="#rateTo" title="Manage costs" data-toggle="collapse">
                                <em class="icon-users"></em>
                                <span>Rates</span>
                            </a>
                            <ul id="rateTo" class="nav sidebar-subnav collapse">
                                <li class=" ">
                                    <router-link to="">
                                                <em class="fa fa-cc"></em>
                                                <span>Origination Rate</span>
                                    </router-link>
                                </li>
                                <li class=" ">
                                    <router-link to="/term_rates">
                                            <em class="fa fa-cc"></em>
                                            <span>Termination rate</span>
                                    </router-link>
                                </li>
                            </ul>
                        </li>
                <li class=" ">
                    <router-link to="/admin/payments">
                        <em class="fa fa-credit-card"></em>
                        <span>Payments</span>
                    </router-link>
                </li>
                <!--<li class=" ">
                    <router-link to="/config">
                                <em class="fa fa-cog"></em>
                                <span>Config</span>
                    </router-link>
                </li>-->
            </ul>
            <!-- END sidebar nav-->
        </nav>
    </div>
    <!-- END Sidebar (left)-->
</aside>            <section>
        <div class="content-wrapper">
            <div class="content-heading">
                Origination rates
                <small> Manage Origination rates </small>
            </div>
                        <div class="container-fluid">
                    <div class="row">
        <div class="col-lg-12">
            <br>
            <div class="panel panel-default">
                <div class="panel-body">
                    <div id="table_wrapper" class="dataTables_wrapper form-inline no-footer">
                        <!--<div class="dt-buttons">
                            <a class="dt-button btn btn-primary" tabindex="0" aria-controls="table">
                                <span>Export to CSV</span>
                            </a>
                        </div>-->
                        <div id="table_filter" class="dataTables_filter">
                            <label>Search by Name:<input v-model="searchNname" autofocus class="form-control input-sm" aria-controls="table"></label>
                        </div>
                        <div id="table_processing" class="dataTables_processing" style="display: none;">Processing...</div>
                        <table id="table" class="table table-striped table-hover  dataTable no-footer" role="grid" aria-describedby="table_info" style="width: 1291px;">
                        <thead>
                        <tr role="row">
                            <th class=""   tabindex="0" aria-controls="table" rowspan="1" colspan="1" aria-label="Country: activate to sort column ascending" style="width: 215px;" >Country</th>
                            <th class="" tabindex="0" aria-controls="table" rowspan="1" colspan="1" aria-label="Destination: activate to sort column ascending" style="width: 641px;">Code Name</th>
                            <th class="sorting" v-bind:class="{ sorting_desc: sortCode }" tabindex="0" aria-controls="table" rowspan="1" colspan="1" aria-label="Code: activate to sort column ascending" style="width: 88px;"  v-on:click="sortByCode()">Code</th>
                            <th class="" tabindex="0" aria-controls="table" rowspan="1" colspan="1" aria-sort="descending" aria-label="Opentact Sell Rate: activate to sort column ascending" style="width: 259px;">Opentact Sell Rate</th>
                        </tr>
                        </thead>
                        <tbody>
                            <tr role="row" class="odd" v-for="listRates in paginate">
                                <td>{{ listRates.country }}</td>
                                <td>{{ listRates.code_name }}</td>
                                <td>{{ listRates.code }}</td>
                                <td class="sorting_1">
                                    <div class="form-group">
                                        <input class="form-control ratesEdit" step="0.01" v-bind:id="listRates.code" style="width: 80px" v-bind:value="listRates.rate" type="number"   name="rateName">
                                    </div>
                                    <a  title="Change opentact rate" class="btn btn-success add_rate_btn btn-sm" v-on:click="changeRate(listRates.code)">
                                        <span class="fa fa-check"> </span>
                                    </a>
                                </td>
                            </tr>
                        </tbody>
                    </table><div class="dataTables_info" id="table_info" role="status" aria-live="polite">Showing {{countStart}} to {{countShow}} of {{ratesCount}} entries</div><div class="dataTables_paginate paging_simple_numbers" id="table_paginate">
                        <ul class="pagination">
                            <li class="paginate_button previous " v-bind:class="{disabled: currentPage === 1 || currentPage === 0}" aria-controls="table" tabindex="0" id="table_previous">
                                <a v-on:click="previousPage()">Previous</a>
                            </li>
                            <li  class="paginate_button active" aria-controls="table" v-for="pageNumber in totalPages" v-if="Math.abs(pageNumber - currentPage) < 3 || pageNumber == totalPages - 1 || pageNumber == 0">
                                <a  class="newPaging" v-on:click="setPage(pageNumber)"  :class="{current: currentPage === pageNumber || pageNumber === 0, last: (pageNumber == totalPages - 1 && Math.abs(pageNumber - currentPage) > 3), first:(pageNumber == 0 && Math.abs(pageNumber - currentPage) > 3)}">{{ pageNumber }}</a>
                            </li>
                            <li class="paginate_button next"  v-bind:class="{disabled: currentPage == totalPages}"  aria-controls="table" tabindex="0" id="table_next">
                                <a v-on:click="nextPage()" >Next</a>
                            </li>
                        </ul> 
                    </div></div>
                </div>
            </div>
        </div>
    </div>
    <input type="hidden" name="_token" value="7JEuNwetDKccbS2b1Wk676gHcTWztb4JWnMJi09A">            </div>
        </div>
    </section>
    <footer>
        <span>Opentact © 2015</span>
    </footer>
</div>
</div>
</template>

<script>

    import Vue from 'vue'
    import VueRouter from 'vue-router'
    import VueResource from 'vue-resource'
    import VeeValidate from 'vee-validate'
    import axios from 'axios'

	import config from '../../config.js'

 
Vue.use(VueRouter)
Vue.use(VueResource)
Vue.use(VeeValidate);

// local storge's***

var newAuthadmin = localStorage.getItem("newAuthadmin");

// var config = {
//   api: 'http://149.56.96.236',
//   port: ':8002/'
// };

    export default {
       name: 'wrapper',
       data() {  
          return {
             ratesArray: [],
             searchNname: '',
             ratesCount:0,
             rate: '',
             mark:0,
             mark_two:2,
             cont: [],
             sortCode: false,
             currentPage: 1,
             itemsPerPage: 10,
             resultCount: 0,
             startIndex: 0,
             endIndex: 10,
             countShow: 0,
             developersCount: 10,
             oldpageNumber: 1,
             countStart: 1,
             checkSearch: true,
          } 
    },
    computed: {
        totalPages: function() {
            if(this.searchNname == ''){
                
                if (this.endIndex >= this.ratesCount){
                    this.countShow = this.ratesCount;
                }
                else{
                        this.countShow = this.endIndex;
                }
                this.itemsPerPage = this.developersCount;
                return Math.ceil(this.ratesCount / this.itemsPerPage)
            }
            else{
                if (this.endIndex >= this.newArray3Len){
                    this.countShow = this.newArray3Len;
                }
                else{
                    this.countShow = this.endIndex;
                }
                this.itemsPerPage = this.developersCount;
                return Math.ceil(this.newArray3Len / this.itemsPerPage);
            }

        },
        paginate: function() {
            if(this.searchNname != ''){
                var pagenumber = 1;
                if(pagenumber != this.oldpageNumber && this.checkSearch === true || this.oldpageNumber == 1){
                    this.setPage(1);
                    this.checkSearch = false
                }
                var newArray3 = this.ratesArray
                    .filter(ratesArray => ratesArray.code_name.toLowerCase().indexOf(this.searchNname.toLowerCase()) !== -1)

                    this.newArray3Len = newArray3.length;
                    this.countShow = this.newArray3Len;
                    this.ratesCount = this.newArray3Len;

                    if(this.newArray3Len == 0 || this.ratesCount == 0){
                        this.countStart = 0;
                    }

                    if(this.newArray3Len >= this.developersCount){
                        
                        this.countShow = this.developersCount;
                        this.ratesCount = this.newArray3Len;

                    }
                    else{
                        this.countShow = this.newArray3Len;
                        this.ratesCount = this.newArray3Len;
                    }
                    return newArray3.slice(this.startIndex , this.endIndex );
            }
            else{
                if(this.checkSearch === false ){
                    this.setPage(1);
                    this.checkSearch = true;
                    this.countStart = 1;
                }
                var array2 = this.ratesArray.length;
                this.countShow = array2;
                this.ratesCount = array2;
                return this.ratesArray.slice(this.startIndex , this.endIndex )
            }
            
        }
    },
    created:function(){
        this.getRates();
         var checkAdmin = localStorage.getItem("adminCheckCode");
            if(checkAdmin == 'adminCheckIsSuccess777**'){

            }
            else{
                this.$router.push('/login')
            }
    },
    methods:{
        setPage: function(pageNumber) {
            
                if(pageNumber != this.oldpageNumber){
                    console.log(pageNumber)
                    this.currentPage = pageNumber;

                    var start = pageNumber * this.developersCount;
                    this.startIndex  = start-this.developersCount;
                    this.endIndex = pageNumber*this.developersCount;
                    this.countStart = this.startIndex + 1;
                    this.oldpageNumber = pageNumber;

                    if (this.endIndex >= this.showDev){
                            this.countShow = this.ratesCount;
                    }else{
                            this.countShow = this.endIndex;
                    }  
                }
        
            },
            nextPage: function(){
                console.log(this.currentPage);
                this.currentPage = this.currentPage + 1;
                var start = this.currentPage * this.developersCount;
                this.startIndex  = start-this.developersCount;
                this.endIndex = this.currentPage*this.developersCount;
                this.countStart = startIndex + 1;

                 this.oldpageNumber = this.currentPage

                if (this.endIndex >= this.showDev){

                    this.countShow = this.showDev;
                }else{
                    this.countShow = this.endIndex;
                }
            },
            previousPage: function(){
                 this.currentPage = this.currentPage - 1;
                    var start =this.currentPage * this.developersCount;
                    this.startIndex  = start-this.developersCount;
                    this.endIndex = this.currentPage*this.developersCount;
                    this.countStart = startIndex + 1;

                    this.oldpageNumber = this.currentPage
                    if (this.endIndex >= this.showDev){
                        this.countShow = this.showDev;
                    }else{
                        this.countShow = this.endIndex;
                    }
            },
        getRates:function(){
            this.$http.get(config.api + config.port + "int/origination",{
                headers:{
                    "Content-Type": "application/json",
                    "Authorization": newAuthadmin
                }
            }).then(function(response){
                this.ratesArray = response.body.ret
                this.ratesCount = response.body.ret.length;
                console.log(this.ratesArray);
            })
        },
        changeRate:function(code){
            
            var rateBody = {
                rate: $('#'+code).val(),
                code: code
            };
            console.log( rateBody.rate)
            this.$http.patch(config.api + config.port + "int/origination",rateBody,{
                headers:{
                    "Content-Type": "application/json",
                    "Authorization": newAuthadmin
                }
            }).then(function(response){
                if(response.body.ret == true){
                    this.getRates();                
                }
                console.log(response);
               
            })
        },
        logout:function(){
                localStorage.removeItem('newAuthadmin');
                localStorage.removeItem('DevId');
				localStorage.removeItem('app_uuid');
                localStorage.removeItem('adminCheckCode');				
                this.$router.push("/login");
            },
        sortByCode: function(){
            if (this.sortCode === true){
                    this.sortCode = false;
                    this.ratesArray.reverse();
                }else{
                    this.sortCode = true;
                      function compare(a, b) {
                        var nameA = a.code.toUpperCase(); 
                        var nameB = b.code.toUpperCase();
                        if (nameA < nameB){
                            return -1                         
                        }
                        if (nameA > nameB){
                            return 1                        
                        }
                        // return 0
                    } 
                    this.ratesArray.sort(compare)
                }
        }
    }
}





</script>