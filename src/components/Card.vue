<template>
  <div>
    <div class="card">
      <h2 class="card__title">{{ title }}</h2>
      <p class="card__description">{{ description }}</p>
      <b-button variant="outline-danger">Detalhes</b-button>
    </div>
  </div>
</template>
<script>
export default {
    name : "Card",
    props : {
        title : String,
        description : String
    }
}
</script>
<style>
.card {
background: #FAFAFA;
box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
padding : 30px;
margin : 20px 10px;
display: flex;
flex-direction: column;
align-items : center;
}
.card .card__title{
font-size : 18px;
font-weight : bold;
color : #000000;
}
.card .card__description{
font-size : 14px;
color : #000000;
}
.card .card__btn {
width: 170px;
height : 40px;
border-radius : 6px;
background-color : #C3121C;
color: #FFFFFF;
border: none;
}
</style>
