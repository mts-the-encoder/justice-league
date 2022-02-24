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
        background-color: $greyDark;
        height: 100px;
        font-family: 'JUSTICE LEAGUE', sans-serif;
        padding-bottom: 2rem;
        display: flex;
        justify-content: center;

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
</style>