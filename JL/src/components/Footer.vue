<template>
  <footer>
    <span>Justice League - mts & copy 2022</span>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
footer {
  background-color: $greyDark;
  height: 90px;
  font-family: "JUSTICE LEAGUE", sans-serif;
  padding-bottom: 2rem;
  display: flex;
  justify-content: center;
  @include respond(desktopsmall) {
    font-size: 24px;
  }
}
span {
  color: $greyLight;
  font-weight: bold;
  transition: 0.4s;
  font-size: 30px;
  margin-left: 120px;
  margin-top: 50px;
  @include respond(desktopsmall) {
    font-size: 32px;
  }
  @include respond(mobile) {
      font-size: 16px;
      align-self: center;
      margin-right: 45px;
    }
}
span:hover {
  color: $grey;
}
</style>