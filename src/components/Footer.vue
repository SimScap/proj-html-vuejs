<template>
<div class="container-fluid p-2">
    <div class="row">
        <div class="col-10 footer-container m-auto d-flex justify-content-between">
            <ul>
                <li><img src="/images/logo-sidearea-1.png" alt="maree logo"></li>
                <li>Let's Get Creative</li>
            </ul>           
            <ul>
                <li><a>maree.qode@gmail.com</a></li>
                <li><a>+44645 321 789</a></li>
            </ul>
            <ul>
                <li><a>Avenue d'Auderghem 10</a></li>
                <li><a>1040 Brussels, Belgium</a></li>
            </ul>            
            <ul>
                <li><a>Stay in touch with us</a></li>
                <ul class="social-logos">
                <li><font-awesome-icon :icon="['fab', 'twitter']" /></li>
                <li><font-awesome-icon :icon="['fab', 'pinterest']" /></li>
                <li><font-awesome-icon :icon="['fab', 'facebook']" /></li>
                <li><font-awesome-icon :icon="['fab', 'linkedin']" /></li>
                </ul>             
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
ul{
    list-style-type: none;
}
ul.social-logos{
    display: inline-flex;
}
ul.social-logos li{
    margin-right: 1rem;
}
a{
    position: relative;
    cursor: pointer;
}
a:before{
content: "";
position: absolute;
width: 100%;
height: 2px;
bottom: 0;
left: 0;
background-color: #FFF;
visibility: hidden;
transform: scaleX(0);
transition: all 0.3s ease-in-out;
}
a:hover:before {
visibility: visible;
transform: scaleX(1);
}
</style>

