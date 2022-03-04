<template>
    <footer>
        <span>Justice League - mts & copy 2022</span>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
   * {
       margin: 0;
       padding: 0%;
   }
   footer {
        background-color: $greyDark;
        height: 100px;
        font-family: 'JUSTICE LEAGUE', sans-serif;
        padding-bottom: 2rem;
        display: flex;
        justify-content: center;
        @include respond(desktopsmall) {
       font-size: 24px;
       @include respond(mobile) {
       font-size: 24px;
       margin: 0;
       padding: 0;

   }
   }
    }
        span {
            color: $greyLight;
            font-weight: bold;
            transition: .4s;
            font-size: 30px;
            margin-left: 120px;
            margin-top: 50px;
        }
        span:hover {
            color: $grey;
        }
@media (max-width: 425px) {
  * {
    width: 100%;
  }
}
</style>