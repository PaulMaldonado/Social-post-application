<template>
  <div>
    <div class="card mb-4">
      <h5 class="card-title text-center mt-3">Escribe una publicación para tus amigos</h5>
      <div class="card-body">
        <form @submit.prevent="addPost">
          <div class="form-group mb-3">
            <input type="text" placeholder="Escribir publicación" class="form-control" v-model="title">
          </div>

          <input type="submit" value="Guardar" class="btn btn-primary btn-block">
        </form>
      </div>
    </div>

    
    <div class="card mt-4" v-for="post in posts" :key="post.id">
      <ul class="list-group list-group-flush">
        <li class="list-group-item">
          {{ post.title }}
          
          <div class="form-group">
            <input type="text" class="form-control" v-model="post.title" v-show="editTitle" @keyup.enter="updateTitle">
          </div>

          <button class="btn btn-danger" @click="deletePost">Eliminar</button>
          <button class="btn btn-success" @click="editPost" v-show="!editTitle">Editar</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      posts: [],
      editTitle: false
    }
  },

  methods: {
    addPost() {
      this.posts.push({
        title: this.title
      })

      this.title = ''
    },

    deletePost(index) {
      this.posts.splice(index, 1)
    },

    editPost() {
      this.editTitle = true
    },

    updateTitle() {
      this.editTitle = false
    }
  }
}
</script>
