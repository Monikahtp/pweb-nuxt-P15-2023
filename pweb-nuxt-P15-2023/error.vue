<template>
    <div>
      <transition name="fade" appear>
        <div class="head1 text-center flex">
        </div>
      </transition>
      <transition name="fade-slide" appear>
        <div class="flex text-center open">
          <h1 class="judul">{{ error.statusCode }}</h1>
          <p class="desc">{{ error.message }}</p>
          <button class="btn btn-sm btn-outline-primary" @click="handleClearError">Back Home</button>
        </div>
      </transition>
    </div>
</template>
  
<script setup>
    defineProps(['error'])

    const handleClearError = () => clearError({redirect: '/'}) 
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
font-size: 72px;
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