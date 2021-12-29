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
          <form action="/">
            <input type="text" placeholder="Email">
            <v-btn depressed color="theme_color" large class="rounded-pill btn-custom" dark>Subscribe</v-btn>
          </form>
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
      
      <div class="image_side_container mx-auto mb-12" style="margin-top: 70px;">
        <div class="side">
          <h4 class="small_title"><span></span> PERFACT DESIGN</h4>
          <h2 class="md_title mt-5">
            It’s Everything You’ll Ever Need.
          </h2>
          <p class="text-grey section-sub-title mt-4 line-height">
            Create custom landing pages with Landik that converts more visitors than any website. With lots of unique blocks, you can easily build a page without coding.
          </p>
          <v-btn class="rounded-pill btn-custom mt-5 pl-9 pr-9" x-large color="theme_color" dark depressed>Explore</v-btn>
        </div>
        <div class="side">
          <img src="~/assets/images/features-one.png" class="img-fluid mx-auto d-block">
        </div>
      </div>

      <div class="sec_divider mx-auto mt-12"></div>

      <div class="image_side_container mx-auto" style="margin-top: 70px;">
        <div class="side">
          <img src="~/assets/images/features-two.png" class="img-fluid mx-auto d-block">
        </div>
        <div class="side">
          <h4 class="small_title"><span></span>USER INTERFACE</h4>
          <h2 class="md_title mt-5">
            Unlimited Features Awaiting For You.
          </h2>
          <p class="text-grey section-sub-title mt-4 line-height">
            Create custom landing pages with Landik that converts more visitors than any website. With lots of unique blocks, you can easily build a page without coding.
          </p>
          <v-btn class="rounded-pill btn-custom mt-5 pl-9 pr-9" x-large color="theme_color" dark depressed>Explore</v-btn>
        </div>
      </div>

      <section class="section" id="what-we-do">
        <div id="what-we-do-background">
          <div class="curv_top">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 3000 185.4">
              <path fill="#fff" d="M3000,185.4V0H0v185.4C496.4,69.8,996.4,12,1500,12S2503.6,69.8,3000,185.4z"></path>
            </svg>
          </div>
          <div class="section-main-head mx-auto text-white">
            <h2 class="section-title">
              <span class="slice slice-black"></span>
              What We Do
            </h2>
            <span class="section-sub-title text-white mt-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis eum modi, adipisci facilis.</span>
          </div>
        </div>

        <div class="container">
          <div class="white_boxes">
            <div v-for="(item, index) in what_we_do_items" :key="index" class="row white_box_row">
              <div class="col-md white_box" v-for="(box, box_index) in item" :key="box_index">
                  <div class="row">
                    <div class="col-1 mr-7">
                      <img :src="box.icon" width="44px" height="44px">
                    </div>
                    <div class="col">
                      <h3 class="title">{{box.title}}</h3>
                      <p class="sub_title text-grey">{{box.sub_title}}</p>
                    </div>
                  </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="section" id="fun_boxes" style="margin-top: -74;">
        <div class="section-main-head mx-auto">
          <h2 class="section-title">
            <span class="slice"></span>
            Hosts Like You, Worldwide
          </h2>
          <span class="section-sub-title text-grey mt-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis eum modi, adipisci facilis.</span>
        </div>
        <div class="container mt-8">
          <div class="row">
            <div class="col-md" v-for="(item, index) in fun_boxes" :key="index">
              <div class="fun_box">
                <i :class="item.icon"></i>
                <h3 class="title">{{item.title}}</h3>
                <span class="sub_title text-grey">{{item.sub_title}}</span>
              </div>
            </div>
          </div>
        </div>
      </section>

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
      ],
      what_we_do_items: [
        [
          {
            icon: "https://themesboss.com/oliver/images/icon/pen&ruller.svg",
            title: "Well Documented",
            sub_title: "Ned ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque."
          },
          {
            icon: "https://themesboss.com/oliver/images/icon/code.svg",
            title: "Highly Customizable",
            sub_title: "The point of using Lorem Ipsum is has a normal distribution of letters, as opposed to using."
          },
        ],
        [
          {
            icon: "https://themesboss.com/oliver/images/icon/headphones.svg",
            title: "24/7 Support",
            sub_title: "There are many variations of but the majority have suffered alteration in some form."
          },
          {
            icon: "https://themesboss.com/oliver/images/icon/groupchat.svg",
            title: "Community",
            sub_title: "If you are going to use a Ipsum, you need to be sure there isn't anything in the middle of text."
          },
        ]
      ],
      fun_boxes: [
        {
          icon: "mdi mdi-star",
          title: "4.92/5",
          sub_title: "Average Ratings"
        }
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
