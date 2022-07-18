<template>
  <div>
    <div class="bg-main"></div>
    <div class="py-5">

      <div class="container-lg">
        <h4 class="text-white">Content goes here></h4>
      </div>

    </div>

    <div class="bg-secondary py-4">
      <div class="container-lg">
        <div class="row justify-content-around">

          <div v-for="(element, index) in productsList" 
            :key="index" class="col-2 d-flex justify-content-center align-items-center">

            <img  class="w-25" src='../assets/images/buy-comics-digital-comics.png' :alt="element.name">
            <h5 class="text-uppercase text-white ms-2 fs-6">{{element.name}}</h5>

          </div>

        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'Main',

  data: function(){
    return {
      productsList: [
        {
          name: "digital comics",
          img: "buy-comics-digital-comics",
        },
        {
          name: "dc merchandise",
          img: "buy-comics-merchandise",
        },
        {
          name: "subscription",
          img: "buy-comics-subscriptions",
        },
        {
          name: "comic shop locator",
          img: "buy-comics-shop-locator",
        },
        {
          name: "dc power visa",
          img: "buy-comics-power-visa",
        },
      ]
    }
  },

}
</script>


<style scoped lang="scss">
  @import "../assets/styles/variables.scss";

  .bg-main {
    background-color: $textColor;
  }

  .bg-secondary {
    background-color: $brandColor;
  }
</style>