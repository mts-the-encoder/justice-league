<template>
  <div class="container" :class="background">
    {{ data.background }}>
    <figure class="img">
      <img class="card-img" :src="require(`../assets/img/${data.img}.png`)" />
    </figure>

    <div class="description" :class="{ 'bg-dark': isDarkMode }">
      <h4>História</h4>
      <p class="p1">{{ data.p1 }}</p>
      <p class="p2">{{ data.p2 }}</p>
      <img class="card-svg" src="../assets/svg/aquaman.svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    data: { type: Object, required: true },
    isDarkMode: { type: Boolean, required: true },
  },
  watch: {
    data() {
      console.log(this.data);
    },
  },
};
</script>
<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
.container {
  height: 550px;
  background-color: $yellow;
  width: 400px;
  border-radius: 30px;
  margin: 0 auto;
  margin-bottom: 30px;
  padding-bottom: 10px;
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
  padding: 15px;
  background-color: #fff;
  border-top-right-radius: 40px;
  border-bottom-right-radius: 30px;
  border-bottom-left-radius: 30px;
  display: flex;
  justify-content: center;
  text-align: center;
  flex-direction: column;
  &.bg-dark {
    background-color: #2b2828;
    color: #fff;
    h4 {
      color: #fff;
    }
    .p1 {
      color: #fff;
    }
    .p2 {
      color: #fff;
    }
  }
  h4 {
    padding: 10px;
    color: $greyDark;
    font-size: 20px;
    align-self: flex-start;
    margin-left: 15px;
    position: absolute;
    margin-bottom: 180px;
  }
  p {
    color: $greyDark;
    font-size: 12px;
    padding: 5px;
  }
  .p1 {
    margin-top: 140px;
  }
  .p2 {
    margin-bottom: 80px;
  }
  img {
    height: 10px;
    width: 10px;
  }
}
</style>
