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
        <div class="col-lg-8" v-for="b in blogs">
          <div class="blog-entry d-flex blog-entry-search-item">
            <RouterLink to="/single" class="img-link me-4">
              <img v-if="b.image" :src="b.image" alt="Image" class="img-fluid" style="width: 400px; height: 200px;">
              <img v-else src="~/assets/images/bikaambon.jpg" alt="Default Image" class="img-fluid" style="width: 400px; height: 200px;">
            </RouterLink>
            <div>
              <span class="date">{{ new Date(b.date).toLocaleDateString('en-US', { year: 'numeric', month: 'short', day: 'numeric' }) }} &bullet; <RouterLink to="#">Food</RouterLink></span>
              <h2><RouterLink to="">{{ b.name }}</RouterLink></h2>
              <p>{{ b.isi.split(/\s+/).slice(0, 10).join(" ") }}...</p>
              <p><RouterLink :to="`/blogs/${b.id}`" class="btn btn-sm btn-outline-primary">Read More</RouterLink></p>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>

  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      blogs: []
    }
  },
  methods: {
    async retrieveFormData() {
      // Iterate through localStorage keys
      await axios.get('http://localhost:3100/api/blog')
        .then(response => {
          // Assign the fetched data to the todoList array
          this.blogs = response.data.docs;
          // console.log(this.taskData[0])
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
      
      // console.log("di dalam retrieve", this.taskData)
    }
  },
  async created () {
    await this.retrieveFormData();
    console.log(this.blogs)
    console.log(this.blogs[0])
  },
};

</script>
<style>

</style>