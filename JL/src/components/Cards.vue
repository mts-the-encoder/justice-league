<template>
    <div class="container">
    
        <div class="img">

        </div>
        <div class="description" :class="{ 'bg-dark': isDarkMode }">
            
        </div>
    </div>
</template>

<script>

export default {
    name: "Cards",
  data() {
    return {
      isDarkMode: false,
    };
  },
}
</script>

<style lang="scss">
    
    .container {
        height: 500px;
        background-color: yellow;
        width: 350px;
        border-radius: 30px;
        margin: 0 auto;
        top: 30px;
    }
        .img {
            background-color: red;
            height: 50%;
            width: 100%;
            border-top-right-radius: 30px;
            border-top-left-radius: 30px;
            border-bottom-left-radius: 40px;
        }
        .description {
            height: 50%;
            width: 100%;
            background-color: #FFF;
            border-top-right-radius: 30px;
            border-bottom-right-radius: 30px;
            border-bottom-left-radius: 30px;
            &.bg-dark {
            background-color: $greyDark;
            }
        }
</style>
