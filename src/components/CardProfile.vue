<template>
  <div>
   <div class="col-md-4 col-sm-12 col-lg-4 col-xl-4 col-xxl-4">
          <div class="card" style="width: 18rem;">
            <img :src="imageProfile" alt="image-profile" class="card-img-top">
            <div class="card-body">
              <h5 class="card-title">{{ name }}</h5>
              <h6 class="card-subtitle mb-2 text-muted"></h6>
              <p class="card-text">{{ city }}</p>
              <p class="card-text"><span class="link">{{ linkSite }}</span></p>

              <button class="btn btn-primary btn-block">Editar perfil</button>
            </div>
          </div>
        </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      imageProfile: 'https://cdn.pixabay.com/photo/2017/02/23/13/05/profile-2092113__340.png',
      name: 'JPaulmn',
      city: 'Guadalajara jalisco',
      youDescription: 'Soy desarrollador de software',
      linkSite: 'http://www.techdesign.org',
    }
  }
}
</script>

<style scoped>
  .link {
    color: #1565c0;
  }

  .post-title {
    font-size: 2em;
    text-align: center;
    color: #757575;
    font-weight: bold;
  }
</style>