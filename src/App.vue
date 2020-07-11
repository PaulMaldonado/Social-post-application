<template>
  <div>
    <Navbar />
    <div class="container">
      <div class="row mt-3">
        <div class="col-md-4 col-sm-12 col-lg-4 col-xl-4">
          <CardProfile />
        </div>

        <div class="col-md-8 col-sm-12 col-lg-8 col-xl-8">
          <div>
            <Post />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar';
import CardProfile from './components/CardProfile';
import Post from './components/Post';

export default {
  name: 'App',
  components: {
    Navbar,
    CardProfile,
    Post
  },
}
</script>

<style>
  body {
    background-color: #e0e0e0;
  }
</style>
