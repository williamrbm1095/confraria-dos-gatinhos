<template>
  <div class="about">
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

    <h1>Sobre nós</h1>
  </div>
</template>

<script>
export default {
  name: "About",
  components: {},
  data() {
    return {
      breadcrumb_custom_items: [
        {
          text: "Início",
          to: "/"
        },
        {
          text: "Sobre nós",
          active: true,
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped>
  a {
    text-decoration: none;
  }
</style>