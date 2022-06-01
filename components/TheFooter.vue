<template>
 <!-- Copyright Footer -->
    <!-- footer -->
    <footer class="bg-image bg-footer">
      <div class="container-full p-5 py-1 mt-3">
        <div class="row">
          <div class="col-md-4 col-lg-4 col-12">
            <div class="container-full">
              <div class="row gx-3">
                <div class="col-11 text-end">
                  <p class="text-white farsi-text">
                    {{ footer_data[0].acf.footer_left_text }}
                  </p>
                </div>
                <div class="col-1 text-end text-md-start text-lg-start">
                  <i class="bi bi-geo-alt-fill text-white"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4 col-lg-4 col-12">
            <div class="container-full pe-md-5 pe-lg-5">
              <div class="row gx-3 pe-md-5 pe-lg-5">
                <div class="col-11 text-end">
                  <p class="text-white mt-md-3 mt-lg-3 p-0 m-0">
                    {{ footer_data[0].acf.footer_center_text }}
                   </p>
                </div>
                <div class="col-1 text-end text-md-start text-lg-start mt-md-3 mt-lg-3">
                  <i class="bi bi-telephone text-white"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4 col-lg-4 col-12 pe-md-5 pe-lg-5">
            <div class="container-full">
              <div class="row gx-3">
                <div class="col-11 text-end">
                  <p class="text-white mt-md-3 mt-lg-3 p-0 m-0">
                    {{ footer_data[0].acf.footer_right_text }}
                  </p>
                  <p class="text-white p-0 m-0">
                    {{ footer_data[0].acf.footer_right_text_2 }}
                  </p>
                </div>
                <div
                  class="col-1 text-end text-md-start text-lg-start mt-md-3 mt-lg-3"
                >
                  <i class="bi bi-instagram text-white"></i>
                  <i class="bi bi-telegram text-white"></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <p class="text-white text-center py-4 farsi-text h6 lh-base copyright">
          {{ footer_data[0].acf.footer_copyright }}
      </p>
    </footer>
</template>

<script>
export default {
    props: ['footer_data']
}
</script>

<style scoped>

</style>