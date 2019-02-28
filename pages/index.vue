<template>
  <section class="dashboard">
    <div class="vertical-container">
      <div class="horizontal-container-left">
        <placeholder v-for="track in $store.state.tracks.collection" :key="track.id" :icon="track.icon" :color="track.color"/>
        <placeholder icon="plus" color="#F7F7F7"/>
      </div>
      <div class="horizontal-container-right">
        
      </div>
    </div>
  </section>
</template>

<script>
export default {
    transition: 'dashboard',
  }
</script>

<style>
.dashboard {
  position: absolute; top: 0; bottom: 0; left: 0; right: 0;
  overflow-y: scroll;
  overflow-x: hidden;
}

.vertical-container {
  position: relative; height: 2000px; width: 100%;
}

.horizontal-container-left{
  position: absolute; top: 0; left: 0; bottom: 0; width: 200px;
  border-right: 2px solid #122035;
}
</style>
