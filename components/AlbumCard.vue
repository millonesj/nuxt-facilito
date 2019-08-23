<template>
  <div class="column is-one-quarter">
    <div class="box">
      <h3>{{album.title}}</h3>
      <a href="#">ver más</a>
    </div>
      
  </div>
</template>
<script>
export default {
  name:'AlbumCard',
  props:{
    album: Object
  }

}
</script>
