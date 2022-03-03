<template>
  <header class="header">
    <a href="#" class="logo">Justice League</a>
    <nav class="nav-bar">
        <span id="toggle">MENU</span>
        <ul>
            <li>
            <a href="#">HOME</a>
            </li>
            <li>
            <a href="#">INIMIGOS</a>
            </li>
            <li>
            <a href="#">FILMES</a>
            </li>
            <li>
            <a href="#">CURIOSIDADES</a>
            </li>
            <li>
            <a href="#">SOBRE</a>
            </li>
        </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "header",
};
</script>

<style lang="scss" scoped>
header {
  background-color: $greyDark;
  font-family: "JUSTICE LEAGUE", sans-serif;
  color: $greyLight;
  display: flex;
  justify-content: space-between;
  border-bottom: 2px solid $greyLight;
}
a {
  text-decoration: none;
  color: $greyLight;
  text-shadow: 1px 1px 0px $grey, 1px 1px 0px $grey, 1px 1px 0px $grey,
    1px 0px 0px $grey;
  font-size: 20px;
  transition: 0.4s;
}
a:hover {
  color: $grey;
}
.logo {
  font-size: 60px;
  padding: 40px;
  white-space: nowrap;
   @include respond(desktopsmall) {
       font-size: 32px;
   }
}

/* MENU */
#toggle {
    display: none;
    @include respond(mobile) {
        display: block;
    }
}
ul {
  list-style: none;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-right: 20px;
  @include respond(mobile) {
      font-size: 16px;
      display: none;
      flex-direction: column;
      align-items: flex-start;
      position: absolute;
      right: -20px;
      top: 96px;
      background-color: $greyDark;
      z-index: 100;

      li {
        margin-bottom: 10px;
      }
  }
}
li {
  margin: 0 1rem;
}


</style>