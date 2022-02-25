<template>
    <div class="container" :class="{ 'background-.' : data.background }">
    
        <figure class="img">
            <img class="card-img" :src="require(`../assets/img/${data.img}.png`)" 
           />
        </figure>

        <div class="description" :class="{ 'bg-dark': data.isDarkMode }">
            <h4>História</h4>
            <p class="p1"> {{ data.p1 }} </p>
            <p class="p2"> {{ data.p2 }} </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: {
        data: {type:Object, required:true},
        isDarkMode:{type:Boolean, required:true},
    },
    watch: {
        data() {
            console.log(this.data);
        }
    },
    // computed: {
    //     darkMode() {
    //         return isDarkMode ? '$yellow' : '$blue';
    //     }
    // }
}
</script>

<style lang="scss">
    
    .container {
        height: 550px;
        background-color: $yellow;
        width: 400px;
        border-radius: 30px;
        margin: 0 auto;
    }
        .img {
            height: 50%;
            width: 100%;
            background: $yellow;
            border-top-right-radius: 30px;
            border-top-left-radius: 30px;
            border-bottom-left-radius: 40px;
        }
        .description {
            height: 50%;
            width: 100%;
            background-color: #FFF;
            border-top-right-radius: 40px;
            border-bottom-right-radius: 30px;
            border-bottom-left-radius: 30px;
            display: flex;
            justify-content: center;
            text-align: center;
            flex-direction: column;
            &.bg-dark {
            background-color: $greyDark;
            }
            h4 {
                padding: 10px;
                color: $greyDark;
                font-size: 20px;
                align-self: flex-start;
                margin-left: 15px;
            }
            p {
                padding: 5px;
                color: $greyDark;
                
            }
        }
</style>
