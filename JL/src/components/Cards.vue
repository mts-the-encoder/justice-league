<template>
    <div class="container">
        <div class="img">

        </div>
        <div class="describe">

        </div>
    </div>
</template>

<script>
export default {
    name: "Cards"
}
</script>

<style lang="scss">
    .container {
        height: 500px;
        background-color: yellow;
        width: 350px;
        border-radius: 30px;
        margin: 0 auto;
        top: 50px;
    }
        .img {
            background-color: red;
            height: 50%;
            width: 100%;
            border-top-right-radius: 30px;
            border-top-left-radius: 30px;
            border-bottom-left-radius: 40px;
        }
        .describe {
            height: 50%;
            width: 100%;
            background-color: blue;
            border-top-right-radius: 30px;
            border-bottom-right-radius: 30px;
            border-bottom-left-radius: 30px;
        }
</style>
