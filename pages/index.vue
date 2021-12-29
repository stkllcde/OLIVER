<template>
  <div>
    <section id="home" class="jumbotron">
      <div class="jumbotron-center">
        <v-btn :ripple="false" class="btn-mute rounded-lg mb-7" large color="theme_color" dark depressed>Get Started</v-btn>
        <h1 class="jumbotron-title">
          Powerfull Analytics
          <br>
          Tools For Your Business.
        </h1>
        <span class="text-grey sub_title mt-6">It is a long established fact that a reader by the readable content of a page when looking at its layout.</span>
        <div class="mixed_input_form">
          <input type="text" placeholder="Email">
          <v-btn depressed color="theme_color" class="rounded-pill" dark>Subscribe</v-btn>
        </div>
        <v-btn onclick="window.scrollTo(0, 600)" x-large icon color="theme_color" class="mt-10">
          <v-icon
            class="pt-1"
            color="theme_color"
          >
            mdi-arrow-down
          </v-icon>
        </v-btn>
      </div>
    </section>
    <div class="d-flex justify-space-around mt-14 mb-14">
      <img v-for="(item, index) in brand_items" :key="index" :src="item.image" :alt="item.alt">
    </div>

    <div class="sec_divider mx-auto"></div>

    <section class="section" id="features">
      <div class="section-main-head mx-auto">
        <h2 class="section-title">
          <span class="slice"></span>
          Explore About Our Awesome Features
        </h2>
        <span class="section-sub-title text-grey mt-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis eum modi, adipisci facilis.</span>
      </div>

    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return{
      brand_items: [
        {
          image: "https://themesboss.com/oliver/images/clients/1.png",
          alt: "black swan"
        },
        {
          image: "https://themesboss.com/oliver/images/clients/2.png",
          alt: "quadra"
        },
        {
          image: "https://themesboss.com/oliver/images/clients/3.png",
          alt: "essence"
        },
        {
          image: "https://themesboss.com/oliver/images/clients/4.png",
          alt: "generic"
        },
      ]
    }
  },
  methods: {
    set_scroll(value){
      console.log(window);
    }
  }
}
</script>
