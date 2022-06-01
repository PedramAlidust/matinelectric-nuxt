<template>
  <div>
    <!--- navigation section -->
    <TheHeader :menu_data="menu" />
    <!-- slider section -->
    <div 
   :style="{ 'background-image': `url(${slide[0].acf.slide_image})` }"
    class="bg-image container-full slider_background d-flex justify-content-center">
      <div class="mask" style="background-color: rgba(0, 0, 0, 0.4)">
        <div class="d-flex justify-content-center align-items-center h-100">
          <div class="row align-items-center">
            <div class="col-12 text-center">
              <p class="fw-bold text-white h1">
                {{ slide_info[0].acf.slide_title }}
              </p>
              <p class="text-white fs-4 px-2 pt-3 px-md-0 px-lg-0 pt-md-0 pt-lg-0">
                {{ slide_info[0].acf.slide_short_desc }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- badge section -->
    <div class="container pt-5 p-md-0 p-lg-0">
      <div class="row gy-4 gy-md-0 gy-lg-0">
        <div class="col-lg-4 col-md-4">
          <div
            class="service_background_one pe-4 text-center rounded-5 shadow-4"
          >
            <div class="container">
              <div class="row gx-4">
                <div class="col-10">
                  <p class="fw-bold h4 text-end pt-4">
                    {{ slide_info[0].acf.badge_title_left }}
                  </p>
                  <p class="text-muted text-end badge-desc">
                    {{ slide_info[0].acf.badge_short_desc_left }}
                  </p>
                </div>
                <div class="col-2 text-end pt-4 mt-2">
                  <i class="bi bi-cash h1 badge-color"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-4">
          <div
            class="service_background_one pe-4 text-center rounded-5 shadow-4"
          >
            <div class="container">
              <div class="row gx-4">
                <div class="col-10">
                  <p class="fw-bold h4 text-end pt-4">
                    {{ slide_info[0].acf.badge_title_center }}
                  </p>
                  <p class="text-muted text-end badge-desc">
                    {{ slide_info[0].acf.badge_short_desc_center }}
                  </p>
                </div>
                <div class="col-2 text-end pt-4 mt-2">
                  <i class="bi bi-lightning-charge-fill h1 badge-color"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-4">
          <div
            class="service_background_one pe-4 text-center rounded-5 shadow-4"
          >
            <div class="container">
              <div class="row gx-4">
                <div class="col-10">
                  <p class="fw-bold h4 text-end pt-4">
                     {{ slide_info[0].acf.badge_title_right }}
                  </p>
                  <p class="text-muted text-end badge-desc">
                     {{ slide_info[0].acf.badge_short_desc_right }}
                  </p>
                </div>
                <div class="col-2 text-end pt-4 mt-2">
                  <i class="bi bi-safe h1 badge-color"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- products section -->
    <section class="pt-md-5 pt-lg-5" id="popular" style="direction: rtl;">
      <div class="container py-5">
        <div class="row">
          <div class="col-12 text-center pb-5 pt-4">
            <p class="txt-color h4 fw-bold">
              {{ most_sale_product_info[0].acf.product_title }}
            </p>
            <p class="text-dark h3 pt-1">
              {{ most_sale_product_info[0].acf.product_short_title }}
            </p>
          </div>
        </div>
        <div class="row">
          <div v-for="most_saled_product in most_sale_products" :key="most_saled_product.id" class="col-lg-3 col-md-3 text-center px-5 px-lg-2 px-md-2 pb-5">
            <!-- card container -->
            <div class="shadow rounded-5 pb-5 product-bg">
              <img class="res-img" :src="most_saled_product.acf.product_image" alt="" />
              <p class="fw-bold h5 text-white">{{ most_saled_product.acf.product_title  }}</p>
              <p class="farsi-text text-white">{{ most_saled_product.acf.product_price_ }} هزارتومان</p>
              <a
                href="tel:09122206427"
                role="btn"
                class="btn btn-color fw-bold text-black bg-light"
              >
                سفارش
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- discount picture -->
    <div class="container py-md-5 py-lg-5 mb-5">
      <div class="row gx-lg-5 gx-md-5 p-3 p-lg-0 p-md-0">
        <div class="col-md-7 col-lg-7">
          <div class="container-full">
            <p
              class="txt-color h4 fw-bold text-center text-md-end text-lg-end pt-lg-3 pt-md-3"
            >
           {{ quality_products[0].acf.quality_product_title }}
            </p>
            <p class="text-dark h4 text-center text-md-end text-lg-end pb-5">
           {{ quality_products[0].acf.quality_product_short_desc }}
            </p>
            <div class="row">
              <div
                class="col-lg-6 col-md-6 text-center px-5 px-lg-3 px-md-3 pb-5"
              >
                <div class="shadow rounded-5 p-3 product-bg">
                  <img class="w-100" :src="quality_products[0].acf.quality_product_left_image" alt="" />
                  <p class="fw-bold h5 text-white">{{ quality_products[0].acf.quality_left_product_title }}</p>
                  <p class="farsi-text text-white">{{ quality_products[0].acf.quality_left_product_price }} </p>
                  <a
                    role="button"
                    href="tel:09122206427"
                    class="btn btn-color fw-bold bg-light"
                  >
                    سفارش
                  </a>
                </div>
              </div>
              <div class="col-lg-6 col-md-6 px-5 px-lg-3 px-md-3 pb-5">
                <div class="shadow rounded-5 p-3 text-center product-bg">
                  <img
                    class="w-100"
                    :src="quality_products[0].acf.quality_product_right_image"
                    alt=""
                  />
                  <p class="fw-bold h5 text-white">{{ quality_products[0].acf.quality_right_product_title }}</p>
                  <p class="farsi-text txt-color text-white">{{ quality_products[0].acf.quality_right_product_price }}</p>
                  <a role="button" href="tel:09122206427" class="btn btn-color fw-bold bg-light">
                    سفارش
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-5 col-lg-5">
          <div class="bg-image best_product_bg rounded-5"
           :style="{ 'background-image': `url(${quality_products[0].acf.quality_product_baner_})` }">
            <div class="mask" style="background-color: rgba(48, 89, 140, 0.9)">
              <div
                class="d-flex justify-content-center align-items-center h-100"
              >
                <div class="row align-items-center">
                  <div class="col-12 text-center">
                    <p class="fw-bold text-white h2 mt-5 pt-5">
                     {{ quality_products[0].acf.quality_product_baner_title }}
                    </p>
                    <p class="text-white h5 pt-4 text-justify pb-2 p-5 lh-base">
                       {{ quality_products[0].acf.quality_product_baner_desc }}
                    </p>
                  <a role="button" href="tel:09122206427" class="btn btn-color fw-bold bg-light">
                    سفارش
                  </a>
                    <div class="pt-5">
                      <img
                        class="img-size"
                        src="/assets/pictures/white-lamp.png"
                        alt=""
                      />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- discount section -->
    <section class="off-bg py-5">
      <div class="container">
        <div class="row gy-5">
          <div v-for="off_product in off_products" :key="off_product.id" class="col-md-6 col-lg-6">
            <div class="discount-bg rounded-5">
              <!-- discount-content -->
              <div class="container">
                <div class="row">
                  <div class="col-8 py-4 text-end">
                    <p class="text-white fw-bold h4">
                      {{ off_product.acf.off_product_short_desc }}
                    </p>
                    <p class="text-white py-2">
                      {{ off_product.acf.off_product_text }}
                    </p>
                    <a
                      :href="off_product.acf.off_button_link"
                      role="button"
                      class="btn btn-sm btn-light fw-bold text-dark"
                    >
                      {{ off_product.acf.off_product_button_text }}
                    </a>
                  </div>
                  <div class="col-4 py-4">
                    <img class="w-100" :src="off_product.acf.off_product_image" alt="" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- call to action -->
    <section class="bg-image cta-bg" :style="{'background-image': `url(${cta[0].acf.product_cta_background})`}">
      <div class="mask" style="background-color: rgba(0, 0, 0, 0.7)">
        <div class="d-flex justify-content-center align-items-center h-100">
          <div class="row align-items-center">
            <div class="col-12 text-center">
              <p class="fw-bold cta-txt-color h5 pb-4 pb-md-0 pb-lg-0">
                {{ cta[0].acf.product_cta_text_one }}
              </p>
              <p class="text-white fs-4 pt-3 d-none d-md-block d-lg-block">
                {{ cta[0].acf.product_cta_text_two }}
              </p>
              <p
                class="cta-desc-color pb-4 farsi-text cta-txt-position px-5 px-lg-0 px-md-0"
              >
                {{ cta[0].acf.product_cta_text_three }}
              </p>
              <a
                :href="cta[0].acf.product_cta_button_link"
                role="button"
                class="btn btn-light fw-bold text-dark"
              >
                {{ cta[0].acf.product_cta_botton_text }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- blog section -->
    <section class="py-5 my-md-5 my-lg-5">
      <div class="container">
        <div class="row">
          <div class="col-12 text-center py-5 py-md-0 py-lg-0">
            <p class="txt-color h4 fw-bold">{{ blog_detail[0].acf.blog_text_one }}</p>
            <p class="text-dark h3 pt-1">{{  blog_detail[0].acf.blog_text_two  }}</p>
          </div>
        </div>
      </div>
      <div class="container py-lg-5 py-md-5 px-5 px-md-0 px-lg-0">
        <div class="row">
          <div v-for="post in posts" :key="post.id" class="col-md-4 col-lg-4">
            <img
              class="w-100 blog-img rounded-5"
              :src="post.acf.post_image"
              alt=""
            />
            <p class="text-end pt-4 fw-bold farsi-text">
              {{ post.acf.post_title }}
            </p>
            <p class="text-muted text-end farsi-text blog-desc">
              {{ post.acf.post_details }}
            </p>
          </div>  
        </div>
      </div>
    </section>
    <!-- footer -->
    <TheFooter :footer_data="copyright" />
  </div>
</template>

<script>
import axios from "axios";
import TheHeader from "@/components/Navigation/TheHeader";
import TheFooter from "@/components/TheFooter";
export default {
  components: {
    TheHeader,
    TheFooter,
  },
  asyncData(context) {
    const menu = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/menu"
    );
    const slider = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/slide"
    );
    const slide_info = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/slide_badge"
    );
    const most_sale_product_info = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/product_title"
    );
    const most_sale_products = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/best_products?per_page=100"
    );
    const quality_products = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/quality_products"
    );
    const off_products = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/off_product"
    );
    const cta = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/product_cta"
    );
    const blog_detail = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/blog_detail"
    );
    const copyright = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/footer"
    );
    const posts = axios.get(
      "https://api.matinelectric.com/wp-json/wp/v2/main_page_posts"
    );

    return axios
      .all([
        menu,
        slider,
        slide_info,
        most_sale_product_info,
        most_sale_products,
        quality_products,
        off_products,
        cta,
        blog_detail,
        copyright,
        posts
      ])
      .then(
        axios.spread((...responses) => {
          const menu = responses[0];
          const slider = responses[1];
          const slide_info = responses[2];
          const most_sale_product_info = responses[3];
          const most_sale_products = responses[4];
          const quality_products = responses[5];
          const off_products = responses[6];
          const cta = responses[7];
          const blog_detail = responses[8];
          const copyright = responses[9];
          const posts = responses[10];

          return {
            menu: menu.data,
            slide: slider.data,
            slide_info: slide_info.data,
            most_sale_product_info: most_sale_product_info.data,
            most_sale_products: most_sale_products.data,
            quality_products: quality_products.data,
            off_products: off_products.data,
            cta: cta.data,
            blog_detail: blog_detail.data,
            copyright: copyright.data,
            posts: posts.data
          };
        })
      )
      .catch((e) => {
        context.error(e);
      });
  },
};
</script>


<style scoped>
/*slide component style */
.slider_background {
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  min-height: 80vh;
  z-index: -1;
}

@media (max-width: 980px) {
  .slider_background {
    min-height: 80vh;
  }
}

@media (max-width: 768px) {
  .slider_background {
    min-height: 70vh;
    background-position: top left !important;
  }
}

.badge-color {
  color: #1c4b84;
}

.badge-desc {
  margin-top: -5px;
}

.best_product_bg {
  background-repeat: no-repeat;
  background-position: top right !important;
  min-height: 700px;
}

/* cta background */
.cta-bg {
  background-repeat: no-repeat;
  background-position: top right !important;
  min-height: 350px;
  background-attachment: fixed;
}

.cta-txt-color {
  color: #e4c412;
}

.cta-desc-color {
  color: #d7d8da;
}

.cta-txt-position {
  margin-top: -10px;
}

</style>
