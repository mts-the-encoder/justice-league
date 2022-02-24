<template>
    <header class="header">
        <a href="#" class="active">Justice League</a>
        <nav class="nav-bar">
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
    name: "header"
}
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';
@import '@/assets/scss/_fonts.scss';
@import '@/assets/scss/_variables.scss';
@import '@/assets/scss/_reset.scss';

header {
    background-color: $greyDark;
    font-family: 'JUSTICE LEAGUE', sans-serif;
    color: $greyLight;
    display: flex;
    justify-content: space-between;
    border-bottom: 2px solid $greyLight;
    }
    a {
        text-decoration: none;
        color: $greyLight;
          text-shadow: 
               1px 1px 0px $grey, 
               1px 1px 0px $grey,                    
               1px 1px 0px $grey,                  
               1px 0px 0px $grey;
        font-size: 20px;
        transition: .4s;
    }
    a:hover {
        color: $grey;
    }
    .active {
        font-size: 60px;
        padding: 40px;
    }
    ul {
        list-style: none;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-right: 20px;
    }
    li {
        margin: 0 1rem;
    }
</style>