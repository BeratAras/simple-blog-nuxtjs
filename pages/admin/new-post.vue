<template>
  <div>
    <PostForm title="Yeni Köşe Yazısı" @submit="savePost($event)" />
  </div>
</template>

<script>
import PostForm from "~/components/admin/PostForm";
export default {
  components: {PostForm},
  methods: {
    savePost(post){
      console.log(post)
    }
  }
}
</script>

<style scoped>

</style>
