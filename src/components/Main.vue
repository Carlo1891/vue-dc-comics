<template>
  <div class="bg-main">
    <div>
      <Jumbotron/>

      <div class="container-lg position-relative py-4">

        <div class="text-uppercase text-white my_title position-absolute">
          Current series
        </div>

        <div class="row mt-4">
          <ComicCard v-for="(comic, index) in comicsList" :key="index" :object="comic"/>
        </div>

        <div class="d-flex justify-content-center">

          <div class="text-uppercase text-white my_button">
            Load More
          </div>

        </div>
      </div>
    </div>

    <div class="bg-secondary py-4">
      <div class="container-lg">
        <div class="row justify-content-around">

          <div v-for="(element, index) in productsList" :key="index" class="col-2 d-flex justify-content-center align-items-center">
            <img  class="w-25" :src="`/img/${element.img}`" :alt="element.name">
            <h5 class="text-uppercase text-white ms-2 fs-6">{{element.name}}</h5>
          </div>

        </div>
      </div>
    </div>

  </div>
</template>

<script>
import Jumbotron from './Jumbotron.vue';
import ComicCard from './ComicCard.vue';

export default {
  name: 'Main',
  components: {
    Jumbotron,
    ComicCard,
  },

  data: function(){
    return {
      comicsList : 
      [
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ],

      productsList: [
        {
          name: "digital comics",
          img: "buy-comics-digital-comics.png",
        },
        {
          name: "dc merchandise",
          img: "buy-comics-merchandise.png",
        },
        {
          name: "subscription",
          img: "buy-comics-subscriptions.png",
        },
        {
          name: "comic shop locator",
          img: "buy-comics-shop-locator.png",
        },
        {
          name: "dc power visa",
          img: "buy-dc-power-visa.svg",
        },
      ],
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
  .my_title {
    font-weight: bold;
    font-size: 2rem;
    text-align: center;
    padding: 10px;
    top: -28px;
    left: 0;
    background-color: $brandColor;
  }
  .comic-card img {
    object-fit: cover;
    height: 200px;
    width: 100%;
    object-position: top;
  }

  .my_button {
    background-color: $brandColor;
    padding: 10px 50px ; 
    align-self: center;
    &:hover {
      cursor: pointer;
    }
  }

</style>