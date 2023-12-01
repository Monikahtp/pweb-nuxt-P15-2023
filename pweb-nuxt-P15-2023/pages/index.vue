<template>
  <div>
    <transition name="fade" appear>
      <div class="head1 text-center flex">
      </div>
    </transition>
    <transition name="fade-slide" appear>
      <div class="flex text-center open">
        <h1 class="judul">Welcome To Our Blogs</h1>
        <p class="desc">Enjoy Our Blogsite</p>
        <p><RouterLink to="/blogs" class="btn btn-sm btn-outline-primary">To Blogs</RouterLink></p>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
};
</script>

<style>
.head1 {
  background-image: url('~/assets/images/bikaambon.jpg');
  width: 100vw;
  height: 100vh;
  background-size: cover;
  background-repeat: no-repeat;
  opacity: 0.5;
}

.judul{
  color: #214252ff;
  font-size: 68px;
}

.open {
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.desc{
  color:rgb(57, 92, 109);
  font-size: 36px;
}

.fade-enter-active, .fade-leave-active, .fade-slide-enter-active, .fade-slide-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to, .fade-slide-enter, .fade-slide-leave-to {
  opacity: 0;
}
</style>