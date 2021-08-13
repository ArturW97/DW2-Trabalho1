<template>
  <header class="header">
    <div class="container">
      <div class="row">
        <div class="col-md-6 ">
          <h1 class="logo">
            <img class="logo__img" src="../assets/LogoSOAD.jpg" />
          </h1>
        </div>
        <div class="col-md-6 header__right">
          <p class="header__text">
            Feito por Artur Wiederkehr, aluno da Professora Zalba Monteiro
          </p>
          <nav class="menu">
            <ul>
              <li><router-link to="/">Home</router-link></li>
              <li>Biografia</li>
              <li><router-link to="/noticias">Notícias</router-link></li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style>
.header {
  background-color: black;
  height: 80px;
  width: 100%;
}
.header__right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}
.logo {
  width: 200px;
  padding: 0px;
  margin-top: 15px;
}
.logo__img {
  width: 100%;
}
.header__text {
  color: #e2e2e2;
  font-size: 10px;
  font-style: italic;
  margin: 8px;
  font-weight: 700;
}
.menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
  color: #e2e2e2;
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
}
.menu ul li {
  padding: 4px 14px;
  font-size: 16px;
  text-transform: uppercase;
  font-weight: 900;
  letter-spacing: 0.5px;
}
.menu ul li:not(:last-child):after {
  content: "";
  display: inline-block;
  width: 1px;
  background-color: #e2e2e2;
  height: 13px;
  margin-left: 20px;
}
.menu ul li:hover {
  background-color: #333;
}
</style>