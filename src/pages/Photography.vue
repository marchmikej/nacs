<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/aerial_photo_pool.jpg')"
      >
      </parallax>
      <div class="container">
        <h1 class="title">Photography</h1>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="row">
            <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                    <div class="col-md-6">
                    <img src="/img/aerial_photo_pool.jpg" class="img-raised" />
                    <img src="/img/bridges.jpg" alt="" class="img-raised" />
                    </div>
                    <div class="col-md-6">
                    <img src="/img/giApartments.jpg" alt="" class="img-raised" />
                    <img src="/img/city_view_1.jpg" alt="" class="img-raised" />
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                    <div class="col-md-12">
                        <video class="col-md-12" controls>
                            <source src="/video/IMG_0062.MP4" type=video/mp4>
                        </video>
                    </div>
                </div>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

export default {
  name: 'photography',
  bodyClass: 'profile-page',
  components: {
  }
};
</script>
<style></style>
