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
      <div class="mt-4">
        <h4>Left and Right (or Start and End)</h4>
        <b-card
          img-src="https://placekitten.com/300/300"
          img-alt="Card image"
          img-left
          class="mb-3"
        >
          <b-card-text>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius dolor, assumenda dolorum ab numquam tenetur. Quae sunt error, optio labore ullam repellendus aliquid excepturi fugit repellat facilis! Officia, sunt quisquam.
          </b-card-text>
        </b-card>
      </div>
    </b-container>
    <!-- This block is a first sector --end-- -->
    <!-- This block is a second sector --start-- -->
    <b-container fluid class="sector sector-2">
      <b-card img-src="https://placekitten.com/300/300" img-alt="Card image" img-right>
        <b-card-text>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi quia voluptatibus officiis tenetur! Ullam ipsam, explicabo cupiditate quas officiis libero reiciendis et neque laboriosam impedit, dolores rerum quibusdam vero perspiciatis!
        </b-card-text>
      </b-card>
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
