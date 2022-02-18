<template>
  <!-- This block is content page --start-- -->
  <div class="home">
    <!-- This block is a breadcrumb component --start-- -->
    <template>
      <div class="breadcrumb">
        <b-breadcrumb>
          <b-breadcrumb-item
            v-for="(val, inx) in breadcrumb_custom_items"
            :to="val.to"
            :active="val.active"
            :key="inx"
          >
            <span style="color: pink" v-if="val.text === 'Blog'">
              {{ val.text }}
            </span>
            <template v-else>
              {{ val.text }}
            </template>
          </b-breadcrumb-item>
        </b-breadcrumb>
      </div>
    </template>
    <!-- This block is a breadcrumb component --end-- -->
    <!-- This block is a title --start-- -->
    <h1>Início</h1>
    <!-- This block is a title --end-- -->
    <!-- This block is a first sector --start-- -->
    <b-container fluid class="sector sector-1">
  
      <b-row cols="1" cols-sm="2" cols-md="2" cols-lg="2" cols-xl="2">
        <b-col> <b-img src="https://placekitten.com/1000/500" fluid alt="Responsive image"></b-img></b-col>
        <b-col><p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam vel veritatis error consequuntur? Error labore et, quo beatae temporibus, veniam repudiandae vitae illo cumque deserunt numquam animi unde magnam tempora.</p></b-col>
      </b-row>

    </b-container>
    <!-- This block is a first sector --end-- -->
    <!-- This block is a second sector --start-- -->
    <b-container fluid class="sector sector-1">
     
      <b-row cols="1" cols-sm="2" cols-md="2" cols-lg="2" cols-xl="2">
        <b-col><p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam vel veritatis error consequuntur? Error labore et, quo beatae temporibus, veniam repudiandae vitae illo cumque deserunt numquam animi unde magnam tempora.</p></b-col>
        <b-col> <b-img src="https://placekitten.com/1000/500" fluid alt="Responsive image"></b-img></b-col>
      </b-row>

    </b-container>
    <!-- This block is a second sector --end-- -->
    <!-- This block is a third sector --start-- -->
    <b-container fluid class="sector sector-3">
      <b-carousel
        id="carousel-1"
        :interval="5000"
        controls
        background="transparent"
        img-width="1024"
        img-height="200"
        style="text-shadow: 1px 1px 2px #333"
      >
        <!-- Slides with image only -->
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
            </b-card-group>
          </template>
        </b-carousel-slide>
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
            </b-card-group>
          </template>
        </b-carousel-slide>
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
              <b-card img-src="https://placekitten.com/300/100" overlay></b-card>
            </b-card-group>
          </template>
        </b-carousel-slide>
      </b-carousel>
    </b-container>
    <!-- This block is a third sector --end-- -->
  </div>
  <!-- This block is content page --end-- -->
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      /* This script block is a return prop of breadcrumb --start-- */
      breadcrumb_custom_items: [
        {
          text: "Início",
          active: true,
        },
      ],
      /* This script block is a return prop of breadcrumb --end-- */
    };
  },
};
</script>

<style lang="css" scoped>
a {
  text-decoration: none;
}
.sector {
  margin-bottom: 30px;
}
.card {
  border: 0 !important;
  margin: 10px;
}
</style>
