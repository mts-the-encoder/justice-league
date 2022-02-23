<template>
    <footer>
        <span>Justice League - mts & copy 2022</span>
    </footer>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';
@import '@/assets/scss/_fonts.scss';
@import '@/assets/scss/_variables.scss';
@import '@/assets/scss/_reset.scss';  

   footer {
        border-bottom: 5px solid $marine;
        background-color: $blue;
        height: 100px;
        font-family: 'JUSTICE LEAGUE', sans-serif;
        padding-bottom: 2rem;
        display: flex;
        justify-content: center;
        
    }
        span {
            color: $red;
            font-weight: bold;
            transition: .4s;
            font-size: 30px;
            padding: 50px;
            margin-left: 120px;
        }
        span:hover {
            color: $greyLight;
        }
</style>