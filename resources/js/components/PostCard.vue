<template>
  <div class="card text-center m-3" style="width: 20rem;">
    <div class="card-header"> {{ post.user.name }} </div>
    <div class="card-body">
      <h5 class="card-title"> {{ post.title }} </h5>
      <p class="card-text">
        {{ post.post_content }}
      </p>
    </div>
    <div class="card-footer text-muted"> {{ post.post_date }} </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
};
</script>

<style>
</style>