<template>
  <div class="card text-center m-3" style="width: 20rem;">
    <div class="card-header"> {{ post.user.name }} </div>
    <div class="card-image p-2">
        <img v-if="isValidURL(post.post_image)" :src="post.post_image" class="card-img-top" :alt="post.title">
        <img v-else :src="'storage/' + post.post_image" class="card-img-top w-100" :alt="post.title">
    </div>
    <div class="card-body">
      <h5 class="card-title"> {{ post.title }} </h5>
      <p class="card-text">
        {{ post.post_content.substring(0, 100) }}...
      </p>
      <a href="#" class="btn btn-primary">See More</a>
    </div>
    <div class="card-footer text-muted"> {{ post.post_date }} </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
  methods:{
    isValidURL(string) {
      var regex = /(?:https?):\/\/(\w+:?\w*)?(\S+)(:\d+)?(\/|\/([\w#!:.?+=&%!\-\/]))?/;
      if(!regex .test(string)) {
        return false;
      } else {
        return true;
      }
    },
  }
};
</script>

<style>
</style>