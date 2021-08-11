<template>
  <section class="discografia">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Discografia</h2>
        </div>
      </div>
      <div class="row">
        <div v-for="album in albuns" :key="album.name" class="col-md-3">
          <div class="discografia__card">
            <img :src="album.img" :alt="album.name" />
            <h5 v-text="album.name"></h5>
            <a :href="album.link" target="_blank"> Ouvir </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Discografia",
  data: function () {
    return {
      albuns: [
        {
          name: "System of A Down",
          img: require("../assets/albumSystemOfADown.jpg"),
          link: "https://www.youtube.com/watch?v=WLoygPzMqyA&list=OLAK5uy_lp66bshuy1phaV1b0XUFAYLkNbdrZLSyo",
        },
        {
          name: "Toxicity",
          img: require("../assets/albumToxicity.jpg"),
          link: "https://www.youtube.com/watch?v=s7ZsYe5Uwg0&list=OLAK5uy_kb1yvg1bLW2yKdKxO1qvzGK7pFl9TuFBw",
        },
        {
          name: "Steal This Album!",
          img: require("../assets/albumStealThisAlbum.jpg"),
          link: "https://www.youtube.com/watch?v=2SoAtEMbEDo&list=PLDA015ABEB01FC5E2",
        },
        {
          name: "Mezmerize",
          img: require("../assets/albumMezmerize.jpg"),
          link: "https://www.youtube.com/watch?v=D_RCCXH3PPg&list=PL6ogdCG3tAWjxC_-yv7CrZ4eUdK0Zyv4L",
        },
        {
          name: "Hypnotize",
          img: require("../assets/albumHypnotize.jpeg"),
          link: "https://www.youtube.com/watch?v=tf1xUGRGLtM&list=PL6ogdCG3tAWjNXe0iBWVcBnM5vldVTSjX",
        },
      ],
    };
  },
};
</script>

<style>
.discografia {
  padding: 56px 0;
  background-color: #212121;
  color: #e2e2e2;
}
.discografia h2 {
  padding-bottom: 30px;
}
.discografia__card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 340px;
}
.discografia__card img {
  width: 100%;
  max-width: 193px;
  height: 193px;
}
.discografia__card a {
  display: block;
  width: 70px;
  height: 30px;
  background-color: #e2e2e2;
  color: #212121;
  text-align: center;
  text-decoration: none;
  line-height: 31px;
  margin-top: 10px;
  margin-bottom: 30px;
  border-radius: 6px;
  font-size: 14px;
  font-weight: 900;
}
.discografia__card h5 {
  font-size: 16px;
  text-align: center;
  padding: 0px;
  display: inline-block;
  max-width: 120px;
  margin: auto;
}
</style>
