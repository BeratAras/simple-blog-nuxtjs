<template>
  <div>
    <div class="card mr-3 mb-3 card-success" style="width: 18rem;">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
          content.</p>
        <div class="admin-button-container" v-if="isAdmin">
          <nuxt-link to="/admin/1" class="btn btn-outline-warning btn-sm">Düzenle</nuxt-link>
          <a href="#" class="btn btn-outline-danger btn-sm">Sil</a>
        </div>
        <nuxt-link v-else to="/posts/1" class="btn btn-outline-info btn-sm">Görüntüle</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Post',
  props:{
    isAdmin: {
      required: true,
      type: Boolean,
    }
  }
}
</script>

<style scoped>

</style>
