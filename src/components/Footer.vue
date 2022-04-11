<template>
<div class="container-fluid p-2">
    <div class="row">
        <div class="col-10 footer-container m-auto d-flex justify-content-between">
            <ul>
                <li><img src="/images/logo-sidearea-1.png" alt="maree logo"></li>
                <li>Let's Get Creative</li>
            </ul>           
            <ul>
                <li><a href="#">maree.qode@gmail.com</a></li>
                <li><a href="#">+44645 321 789</a></li>
            </ul>
            <ul>
                <li><a href="#">Avenue d'Auderghem 10</a></li>
                <li><a href="#">1040 Brussels, Belgium</a></li>
            </ul>            
            <ul>
                <li><a href="#">Stay in touch with us</a></li>
                <li>ff</li>
                <li>ff</li>
                <li>ff</li>
                <li>ff</li>
            </ul>
        </div>
    </div>
    </div>  
</template>

<script>
export default {
    name: "FooterContent"

}
</script>

<style  scoped lang="scss">
div.container-fluid{
    background-color: #C0E1CF;
}
div.footer-container{
    border: 2px solid black;
}
ul{
    list-style-type: none;
}
</style>

