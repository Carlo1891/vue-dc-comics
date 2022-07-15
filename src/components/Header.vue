<template>
  <div>
    <nav class="navbar navbar-expand-lg bg-white">

      <div class="container-lg d-flex ">
        <img class="" src="../assets/images/dc-logo.png" alt="dc-logo">
        <div class=" justify-content-end" id="navbarNavAltMarkup">

          <div class="navbar justify-self-end">
            <a class="nav-link active px-3" href="#" v-for="(link, index) in menuList" :key="index">{{link.name}}</a>    
          </div>

        </div>
      </div>

    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header',

  data: function (){
    return {
      menuList: [
        {
          name: 'Characters',
          url: '#',
          active: false,
        },
        {
          name: 'Comics',
          url: '#',
          active: false,
        },
        {
          name: 'Movies',
          url: '#',
          active: false,
        },
        {
          name: 'TV',
          url: '#',
          active: false,
        },
        {
          name: 'Games',
          url: '#',
          active: false,
        },
        {
          name: 'Collectibles',
          url: '#',
          active: false,
        },
        {
          name: 'Videos',
          url: '#',
          active: false,
        },
        {
          name: 'Fans',
          url: '#',
          active: false,
        },
        {
          name: 'News',
          url: '#',
          active: false,
        },
        {
          name: 'Shop',
          url: '#',
          active: false,
        },
      ]
    }
  }

}
</script>

<style scoped lang="scss">
  @import "../assets/styles/variables.scss";

  .container-lg > img{
    width: 80px;
  }

  .navbar {
    padding-bottom: 0px;
    padding-top: 0px;
  }

  .navbar > a {
    color: $textColor;
    font-size: 0.8rem;
    &:hover{
      border-bottom: 5px solid $brandColor;
      color: $brandColor
    }
  }

</style>