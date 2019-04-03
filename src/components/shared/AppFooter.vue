<template>
    <div>
        <footer class="footer">
        <div class="b-container">
            <div class="copyright">
                <p>Всички права запазени | Христо Димитров © 2019</p>
            </div>
            <div class="social">
                <a href="https://www.facebook.com/hristo.dimitrov.7758"><i class="fa fa-facebook"></i></a>
                <a href="https://github.com/Hristoo"><i class="fa fa-github"></i></a>
            </div> 
        </div>

      </footer>
    </div>    
</template>

<script>
export default {
    data(){
        return {
            title: 'This is the Footer'
        }
    }
}
</script>

<style scoped>
    .social{
    font-size: 25px;
    float: right;
    margin-right: 5%;
    color: #fff;
}
i{
    color: #fff;
    margin-right: 5px;
}
.footer{
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    background: #5597b4;
    height: 50px;
    padding: 10px;

}
.copyright{
    float: left;
    padding-top: 5px;
    margin-left: 21%;
    color: #fff;
    text-align: left;
}
    

</style>
