<template>
  <div>
  <div class="hero overlay inner-page bg-primary py-5">
    <div class="container">
      <div class="row align-items-center justify-content-center text-center pt-5">
        <div class="col-lg-6">
          <h1 class="heading text-white mb-3" data-aos="fade-up">Makanan Khas Sumatera Utara</h1>
        </div>
      </div>
    </div>
  </div>

  <div class="section search-result-wrap">
    <div class="container">
      
      <div class="row posts-entry">
        <div class="col-lg-8">
          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img src="~/assets/images/bikaambon.jpg" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">Dec. 2nd, 2023 &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="">Bika Ambon</RouterLink></h2>
              <p>Bika Ambon adalah kue tradisional yang lezat dan populer di daerah Sumatera Utara. Berikut resep</p>
              <p><RouterLink to="/single" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img src="~/assets/images/tauco.jpg" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">Dec. 2nd, 2023 &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="/single">Tauco Udang Sumatera Utara</RouterLink></h2>
              <p>Tauco Udang Medan adalah makanan tradisional yang lezat dan populer di daerah Sumatera Utara.</p>
              <p><RouterLink to="/single" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img src="~/assets/images/teri.jpg" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">Dec. 2nd, 2023 &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="/single">Sambal Pete Teri Medan</RouterLink></h2>
              <p>Sambal Pete Teri Medan adalah makanan tradisional lezat dan populer dari daerah Sumatera Utara.</p>
              <p><RouterLink to="/single" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img src="~/assets/images/soto.jpg" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">Dec. 2nd, 2023 &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="/single">Soto Medan</RouterLink></h2>
              <p>Soto Medan adalah makanan khas daerah, lezat dan sangat populer dari daerah Sumatera Utara. </p>
              <p><RouterLink to="/single" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img src="~/assets/images/daunubi.jpeg" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">Dec. 2nd, 2023 &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="/single">Daun Ubi Tumbuk</RouterLink></h2>
              <p>Daun Ubi Tumbuk adalah makanan tradisional lezat dan populer dari daerah Sumatera Utara.</p>
              <p><RouterLink to="/single" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

          <div class="row text-start pt-5 border-top">
            <div class="col-md-12">
              <div class="custom-pagination">
                <span>1</span>
                <RouterLink to="#">2</RouterLink>
                <RouterLink to="#">3</RouterLink>
                <RouterLink to="#">4</RouterLink>
                <span>...</span>
                <RouterLink to="#">15</RouterLink>
              </div>
            </div>
          </div>

        </div>

        <div class="col-lg-4 sidebar">

          <div class="sidebar-box search-form-wrap mb-4">
            <form action="#" class="sidebar-search-form">
              <span class="bi-search"></span>
              <input type="text" class="form-control" id="s" placeholder="Type a keyword and hit enter">
            </form>
          </div>
          <!-- END sidebar-box -->
          <div class="sidebar-box">
            <h3 class="heading">Popular Posts</h3>
            <div class="post-entry-sidebar">
              <ul>
                <li>
                  <RouterLink to="">
                    <img src="~/assets/images/makan3.png" alt="Image placeholder" class="me-4 rounded">
                    <div class="text">
                      <h4> </h4>
                      <div class="post-meta">
                        <span class="mr-2">March 15, 2018 </span>
                      </div>
                    </div>
                  </RouterLink>
                </li>
                <li>
                  <RouterLink to="">
                    <img src="~/assets/images/makan1.jpg" alt="Image placeholder" class="me-4 rounded">
                    <div class="text">
                      <h4></h4>
                      <div class="post-meta">
                        <span class="mr-2">March 15, 2018 </span>
                      </div>
                    </div>
                  </RouterLink>
                </li>
                <li>
                  <RouterLink to="">
                    <img src="~/assets/images/food.jpg" alt="Image placeholder" class="me-4 rounded">
                    <div class="text">
                      <h4></h4>
                      <div class="post-meta">
                        <span class="mr-2">March 15, 2018 </span>
                      </div>
                    </div>
                  </RouterLink>
                </li>
              </ul>
            </div>
          </div>
          <!-- END sidebar-box -->

          <div class="sidebar-box">
            <h3 class="heading">Categories</h3>
            <ul class="categories">
              <li><RouterLink to="#">Food <span>(12)</span></RouterLink></li>
              <li><RouterLink to="#">Food <span>(15)</span></RouterLink></li>
              <li><RouterLink to="#">Food <span>(21)</span></RouterLink></li>
              <li><RouterLink to="#">Food <span>(25)</span></RouterLink></li>
              <li><RouterLink to="#">Food <span>(26)</span></RouterLink></li>
              <li><RouterLink to="#">Food <span>(27)</span></RouterLink></li>
            </ul>
          </div>
          <!-- END sidebar-box -->

          <div class="sidebar-box">
            <h3 class="heading">Tags</h3>
            <ul class="tags">
              <li><RouterLink to="#">Makan</RouterLink></li>
              <li><RouterLink to="#">Medan</RouterLink></li>
              <li><RouterLink to="#">Food</RouterLink></li>
              <li><RouterLink to="#">Sumatera</RouterLink></li>
              <li><RouterLink to="#">Food</RouterLink></li>
              <li><RouterLink to="#">Sumatera Utara</RouterLink></li>
              <li><RouterLink to="#">Arsik</RouterLink></li>
              <li><RouterLink to="#">Soto Medan</RouterLink></li>
              <li><RouterLink to="#">Food</RouterLink></li>
              <li><RouterLink to="#">Lontong</RouterLink></li>
              <li><RouterLink to="#">Food</RouterLink></li>
              <li><RouterLink to="#">tauco</RouterLink></li>
            </ul>
          </div>

        </div>
      </div>
    </div>
  </div>

  </div>
</template>

<script lang="ts" setup>
// import { SingleBlog } from '~/components/single-blog.vue';
import { RouterLink } from 'vue-router';


</script>
<style>

</style>