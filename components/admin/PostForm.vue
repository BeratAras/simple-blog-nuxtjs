<template>
  <div class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center">
    <form style="width: 500px" @submit.prevent="onsubmit">
      <fieldset>
        <legend>{{ title }}</legend>
        <div class="form-group">
          <label>Yazar Adı</label>
          <input type="text" class="form-control" v-model="post.author" placeholder="Yazarın adını giriniz..">
        </div>
        <div class="form-group">
          <label>Baslık</label>
          <input type="text" class="form-control" v-model="post.title" placeholder="Yazının baslıgını giriniz..">
        </div>
        <div class="form-group">
          <label>Alt Baslık</label>
          <input type="text" class="form-control" v-model="post.subTitle" placeholder="Yazının alt baslıgını giriniz..">
        </div>
        <div class="form-group">
          <label>Köse Yazısı</label>
          <textarea class="form-control" v-model="post.text" rows="5"></textarea>
        </div>
        <button class="btn btn-danger">İptal</button>
        <button type="submit" class="btn btn-primary">Kaydet</button>
      </fieldset>
    </form>
  </div>
</template>

<script>
export default {
  props: ['title'],
  data(){
    return{
      post: {
        title: null,
        subTitle: null,
        author: null,
        text: null,
      }
    }
  },
  methods: {
    onsubmit(){
      this.$emit("submit", this.post);
    }
  }
}
</script>

<style scoped>

</style>
