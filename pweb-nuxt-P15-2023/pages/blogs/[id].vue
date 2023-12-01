<template>
  <div v-if="blog!=null">
    <div :class="{ 'site-cover': true, 'site-cover-sm': true, 'same-height': true, overlay: true, 'single-page': true, head: blog.image !== null }">
    <div class="container">
      <div class="row same-height justify-content-center">
        <div class="col-md-6">
          <div class="post-entry text-center">
            <h1 class="mb-4">{{ blog.name }}</h1>
            <div class="post-meta align-items-center text-center">
              <figure class="author-figure mb-0 me-3 d-inline-block">
                <img :src="blog.image" alt="Image" class="img-fluid" v-if="blog.image">
                <img src="~/assets/images/arsik.png" alt="Image" class="img-fluid" v-else>
              </figure>
              <span class="d-inline-block mt-1">By {{ blog.author }}</span>
              <span>&nbsp;-&nbsp; {{ new Date(blog.date).toLocaleDateString('en-US', { year: 'numeric', month: 'long', day: 'numeric' }) }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <section class="section">
    <div class="container">

      <div class="row blog-entries element-animate">

        <div class="col-md-12 col-lg-8 main-content">
          <div class="post-content-body">

            <div class="row my-4">
              <div class="col-md-12 mb-4">
                <img :src="blog.image" alt="Image placeholder" class="img-fluid rounded" v-if="blog.image">
                <img src="~/assets/images/bikaambon.jpg" alt="Image placeholder" class="img-fluid rounded" v-else>
              </div>

            </div>

            <p>{{ blog.isi }}</p>

            
          </div>
            <!-- END comment-list -->

        </div>

        <!-- END main-content -->
          <!-- END sidebar-box -->
      </div>
        <!-- END sidebar -->

    </div>
  </section>


  
  <!-- End posts-entry -->

  </div>
</template>

<!-- <script>
import axios from 'axios';

export default {
  data() {
    return {
      blog: null
    }
  },
  methods: {
    async retrieveFormData() {
      const {id} = useRoute().params
      // Iterate through localStorage keys
      await axios.get('http://localhost:3100/api/blog/' + id)
        .then(response => {
          // Assign the fetched data to the todoList array
          this.blog = response.data;
          // console.log(this.taskData[0])
        })
        .catch(error => {
          console.log(error)
        });
      
      // console.log("di dalam retrieve", this.taskData)
    }
  },
  async created () {
    await this.retrieveFormData();
    if (this.blog==null){
      console.log("jalan");
      throw createError({ statusCode: 404, statusMessage: 'Blogs Not Found'})
    }
  },
};
</script> -->

<script setup>
  const {id} = useRoute().params
  const url = 'http://localhost:3100/api/blog/' + id
  const {data: blog} = await useFetch(url, {key: id})

  if (!blog.value){
    throw createError({ statusCode: 404, statusMessage: 'Blogs Not Found'})
  }
</script>

// <!-- <script setup>
//     if (this.blog==null){
//       console.log("jalan");
//       throw createError({ statusCode: 404, statusMessage: 'Blogs Not Found'})
//     }
// </script> -->

<style>
.head{
  background-image: url('~/assets/images/hero_5.jpg');
}
</style>