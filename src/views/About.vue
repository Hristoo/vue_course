<template>
    <div>
         
        <img class="img"  :src="img" alt="" /> 
        <h1  class="txt">{{ title }}</h1>
            <p class="txt">Ентусиазиран уеб програмист със силно желание за усъвършенстване.<br />
            Знания, добри комуникативни умения и отговорно отношение към работния процес.<br />
            Екипен играч и бързо учащ се.        </p>
            <p class="txt">
            Имам интереси в  SEO оптимизация и уеб програмиране 
            от начална концепция до окончателното завършване на целия сайт. Имам дълъг 
            списък от професионално изпълнени проекти и този списък продължава да расте всеки ден. 
            Предоставянето на експертно обслужване е моята мисия и разполагам с всички умения и опит, 
            с които да направят това на цена, която наистина бихте харесали..</p>
        
    </div>    
</template>

<script>
export default {
    data(){
        return {
            title: 'Здравейте, това съм аз!',
            img: 'http://hid.thelocalsearches.com/wp-content/uploads/2018/01/Hristo-1.jpg'
        }
    }
}
</script>

<style scoped>
div{
    margin-top: 40px;
}
.img{
    width: 30%;
    height: auto;
    float: left;
    display: inline;
    margin: 5px;

}
.txt{
    float: right;
    width: 60%;
    margin-top: 5px;
    display: inline;
}
</style>
