<template>
    <div class="nav">
        <ul class="nav nav-pills">
            <li class="nav-item">
                <router-link 
                    class="nav-link"
                    to="/"
                    active-class="active"
                    exact><i class="fa fa-home fa-lg"></i> Начало</router-link>
            </li>
            <li class="nav-item">
                <router-link 
                    class="nav-link"
                    to="/about"
                    active-class="active"><i class="fa fa-user fa-lg"></i> За мен</router-link>
            </li>
            <li class="nav-item">
                <router-link 
                    class="nav-link"
                    to="/projects"
                    active-class="active"><i class="fa fa-folder-open fa-lg"></i> Проекти</router-link>
            </li>
            <li class="nav-item">
                <router-link 
                    class="nav-link"
                    to="/contact"
                    active-class="active"><i class="fa fa-envelope fa-lg"></i> Контакти</router-link>
            </li>
        </ul>
    </div>    
</template>

<script>
export default {
    data(){
        return {
            title: 'This is the header'
        }
    }
}
</script>

<style >
   .nav{
    /*display:inline-block;
    margin:60px auto 45px;*/
    width: 100%;
    background-color:#5597b4;
    box-shadow:0 1px 1px #ccc;
    border-radius:2px;
    
}
.nav-pills{
    margin-left: 21%;
}
.nav a{
    display:inline-block;
    padding: 18px 30px;
    color:#fff !important;
    font-weight:bold;
    font-size:16px;
    text-decoration:none !important;
    line-height:1;
    text-transform: uppercase;
    background-color:transparent;

    -webkit-transition:background-color 0.25s;
    -moz-transition:background-color 0.25s;
    transition:background-color 0.25s;
}
   .nav a:first-child{
    border-radius:2px 0 0 2px;
}

.nav a:last-child{
    border-radius:0 2px 2px 0;
}

</style>
