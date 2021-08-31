<template>
  <section class="banner">
    <div class="banner__imgs">
      <img
        class="images"
        :class="{ active: activeFoto1 }"
        src="../assets/SOAD__banner1.jpg"
        alt="foto do banner 1"
      />
      <img
        class="images"
        :class="{ active: activeFoto2 }"
        src="../assets/SOAD__banner2.jpg"
        alt="foto do banner 2"
      />
    </div>
    <div class="container banner__content">
      <div class="row">
        <div class="col-md-10">
          <p>
            Vivamus nec elit eget nulla aliquet eleifend. Praesent finibus
            pulvinar dolor vel ornare. Proin imperdiet ipsum quis mauris viverra
            rhoncus. Aliquam sit amet lacus molestie, faucibus elit nec,
            consequat massa. Aenean tincidunt eros at felis consectetur, in
            sodales sem sagittis. Praesent condimentum magna sit amet libero
            cursus, id porttitor mi tincidunt. Praesent eleifend quis mauris
            porta hendrerit. Donec faucibus nulla non erat viverra, vitae ornare
            risus tincidunt.
          </p>
          <button>Discografia</button>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Banner",
  data: function () {
    return {
      activeFoto1: true,
      activeFoto2: false,
    };
  },
  methods: {
    toMove: function () {
      this.activeFoto1 = !this.activeFoto1;
      this.activeFoto2 = !this.activeFoto2;
    },
  },
  created: function () {
    setInterval(() => {
      this.toMove();
    }, 5000);
  },
  //        created : function(){
  //        setInterval(function(){
  //            this.toMove();
  //        }, 5000)
};
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
.banner__content .row {
  height: 700px;
}
.banner__content {
  position: relative;
}
.banner__content p {
  font-size: 20px;
  line-height: 25px;
}
.banner__imgs {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 700px;
}
.images {
  width: 100%;
  position: absolute;
  top: 0;
  opacity: 0;
  transition: opacity linear 2.5s;
}
.active {
  opacity: 1;
}
.banner__content .row {
  align-items: flex-end;
}
.banner__content p {
  font-size: 20px;
  margin-left: 70px;
  line-height: 25px;
}
.banner__content button {
  font-size: 20px;
  margin-left: 70px;
  width: 170px;
  height: 40px;
  background-color: #e2e2e2;
  color: #212121;
  border: none;
  font-size: 18px;
  font-weight: 900;
  border-radius: 6px;
  margin-bottom: 54px;
}
</style>