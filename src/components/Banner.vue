<template>
    <section class="banner">
        <div class="banner__imgs">
            <img class="images" :class="{'active' : activeFoto1}" src="../assets/SOAD__banner1.jpg"  alt="foto do banner 1"/>
            <img class="images" :class="{'active' : activeFoto2}" src="../assets/SOAD__banner2.jpg"  alt="foto do banner 2"/>
        </div>
        <div class="container banner__content">
            <div class="row">
                <div class="col-md-10">
                    <p>Vivamus nec elit eget nulla aliquet eleifend. Praesent finibus pulvinar dolor vel ornare. 
                        Proin imperdiet ipsum quis mauris viverra rhoncus. Aliquam sit amet lacus molestie, 
                        faucibus elit nec, consequat massa. Aenean tincidunt eros at felis consectetur, in 
                        sodales sem sagittis. Praesent condimentum magna sit amet libero cursus, id porttitor 
                        mi tincidunt. Praesent eleifend quis mauris porta hendrerit. Donec faucibus nulla non 
                        erat viverra, vitae ornare risus tincidunt. Vestibulum et dignissim dolor, sed eleifend 
                        odio. Vestibulum sit amet libero felis. In commodo turpis eget gravida ornare. 
                        Suspendisse auctor tellus vitae erat aliquam volutpat. Nam placerat interdum arcu, eget 
                        tincidunt odio ullamcorper nec. Donec at ipsum ut nisi commodo condimentum.</p>
                    <button>Discografia</button>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
    export default {
        name: "Banner",
        data : function () {
            return{
                activeFoto1 : true,
                activeFoto2 : false
            }
        },
        methods: {
            toMove : function () {
                this.activeFoto1 = !this.activeFoto1;
                this.activeFoto2 = !this.activeFoto2;
            }
        },
        created : function(){
            setInterval(() =>{
                this.toMove();
            }, 5000)
        },
//        created : function(){
//        setInterval(function(){
//            this.toMove();
//        }, 5000)

    }
</script>

<style>
    .banner {
        width: 100%;
        height: 700px;
        background-color: #212121;
        position: relative;
        color: #e2e2e2;
        overflow: hidden;
    }

    .banner__imgs{
        position: absolute;
        top: 0;
        width: 100%;
    }

    .images{
        width:100%;
        position: absolute;
        top: 0;
        opacity: 0;
        transition: opacity linear 2.5s;
    }

    .active{
        opacity: 1;
    }

    .banner__content{
        position: relative;
    }

    .banner__content p{
        font-size: 20px;
        line-height: 25px;
        color: rgb(34, 34, 34);
        font-weight: bold;
    }
</style>