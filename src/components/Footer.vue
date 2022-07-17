<template>
 <div class="bg-main">
      <div class="container-lg">

        <div class="row">
          <div class="col-6 d-flex">
            <div class="col-4 d-flex flex-column py-5">

              <div class="col-12 ">
                <h5 class="text-uppercase text-white mb-2">dc comics</h5>

                <ul>
                  <li v-for="(link, index) in dcComicsList" :key="index" class="footer-li"><a :href="link.url">{{link.name}}</a></li>
                </ul>

              </div>

              <div class='col-12'>
                <h5 class="text-uppercase text-white mb-2">Shop</h5>

                <ul>
                  <li v-for="(link, index) in shopList" :key="index" class="footer-li"><a :href="link.url">{{link.name}}</a></li>
                </ul>

              </div>
            </div>

            <div class="col-4 py-5">
              <h5 class="text-uppercase text-white mb-2">DC</h5>

              <ul>
                <li v-for="(link, index) in dcList" :key="index" class="footer-li"><a :href="link.url">{{link.name}}</a></li>
              </ul>

            </div>

            <div class="col-4 py-5">
              <h5 class="text-uppercase text-white mb-2">Sites</h5>

              <ul>
                <li v-for="(link, index) in sitesList" :key="index" class="footer-li"><a :href="link.url">{{link.name}}</a></li>
              </ul>

            </div>

          </div>

          <div class="col-6 bg-logo d-flex justify-content-end">
            <img src="../assets/images/dc-logo-bg.png" alt="bg logo">
          </div>  

        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'ContentMain',
  data: function() {
    
    return {
      dcComicsList: [
        {
          name: "Character", 
          url: "#",
        },
        {
          name: "Comics", 
          url: "#",
        },
        {
          name: "Movies", 
          url: "#",
        },
        {
          name: "TV", 
          url: "#",
        },
        {
          name: "Games", 
          url: "#",
        },
        {
          name: "Videos", 
          url: "#",
        },
        {
          name: "News", 
          url: "#",
        },
      ],
      shopList: [
        {
          name: "Shop DC", 
          url: "#",
        },
        {
          name: "Shop DC Collectibles", 
          url: "#",
        },
      ],
      dcList: [
        {
          name: "Terms Of Use", 
          url: "#",
        },
        {
          name: "Privacy policy (New)", 
          url: "#",
        },
        {
          name: "Ad Choices", 
          url: "#",
        },
        {
          name: "Advertising", 
          url: "#",
        },
        {
          name: "Jobs", 
          url: "#",
        },
        {
          name: "Subscriptions", 
          url: "#",
        },
        {
          name: "Talent Workshops", 
          url: "#",
        },
        {
          name: "CPSC Certificates", 
          url: "#",
        },
        {
          name: "Ratings", 
          url: "#",
        },
        {
          name: "Shop Help", 
          url: "#",
        },
        {
          name: "Contact Us", 
          url: "#",
        },
      ],
      sitesList: [
        {
          name: "DC", 
          url: "#",
        },
        {
          name: "MAD Magazine", 
          url: "#",
        },
        {
          name: "DC Kids", 
          url: "#",
        },
        {
          name: "DC Universe", 
          url: "#",
        },
        {
          name: "DC Power Visa", 
          url: "#",
        },
      ]
    }

  }
}

</script>
<style scoped lang="scss">

  @import "../assets/styles/variables.scss";

  .bg-main {
    background-image: url(../assets/images/footer-bg.jpg);
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    max-height: 500px;
    z-index: -1;
    overflow-y: hidden;
  }

  .bg-sec {
    background-color: $bgFooter;
    z-index: 1;
  }

  .footer-li {
    padding-left: 0px;
    margin-left: 0px;
  }

  ul {
    list-style: none;
    padding-left: 0px; 
    li{
      padding: 5px 0;
    }
  }

  .bg-logo {
    overflow-y: hidden;
    height: 100%;
    img{
      height: 600px;
      transform: translateY(-50px);
    }
  }

  a{
    color: lightgrey;
    text-decoration: none;
  }
  
  .my_button {
    color: white;
    border: 2px solid $brandColor;
    padding: 10px;
    &:hover{
      cursor: pointer;
    }
  }

  .my_cta {
    color: $brandColor;
  }

</style>