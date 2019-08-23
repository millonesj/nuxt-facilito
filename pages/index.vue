<template>
  <div class="container">
    <h1 class="title">Aqui viene la lista de Albums</h1>
    <div >
      <div class="columns is-multiline">
        <AlbumCard :album="album" v-for="album in albums" :key="album.id"></AlbumCard>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios';
import env from '../config/env';
import AlbumCard from '../components/AlbumCard'
export default {
  name: 'IndexPage',
  components:{
    AlbumCard
  },
  data() {
    return {
      mensaje:'',
      albums:[]
    }
  },
  created (){
    axios.get(`${env.endpoint}/albums`).then(res => {
      this.albums = res.data;
      console.log(res);
    })
  }
  
}
</script>
<style scoped>
  
</style>
/* https://codigofacilito.com/videos/integrar-un-framework-css */
