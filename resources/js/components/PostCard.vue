<template>
  <div class="card">
    <ul>
        <li>
            {{ post.title }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    props: ['post'],
}
</script>

<style>

</style>