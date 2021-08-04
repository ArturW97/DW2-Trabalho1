<template>
    <section class="banner">
        <div class="banner__imgs">
            <img class="images" :class="{'active' : activeFoto1}" src="../assets/SOAD__banner1.jpg"  alt="foto do banner 1"/>
            <img class="images" :class="{'active' : activeFoto2}" src="../assets/SOAD__banner2.jpg"  alt="foto do banner 2"/>
        </div>
        <div class="container banner__content">
            <div class="row">
                <div class="col-md-10">
                    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum</p>
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
    }
</style>