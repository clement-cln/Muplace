<template>
  <section class="dashboard">
    <div class="vertical-container">
      <div class="horizontal-container-left">
        <placeholder v-touchfeedback v-for="track in $store.state.tracks.collection" :key="track.id" :icon="track.icon" :color="track.color"/>
        <placeholder icon="plus" color="#F7F7F7"/>
      </div>
      <div class="horizontal-scroll">
        <div class="horizontal-container-right">
          <div class="track">

          </div>
          <div class="track"></div>
          <div class="track"></div>
        </div>
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
  z-index: 10;
}

.horizontal-scroll{
  overflow-y: hidden;
  overflow-x: scroll;
}

.horizontal-container-right{
  position: relative; top: 0; left: 200px; bottom: 0; width: 100%;


}

.track {
  position: relative; height: 256px; width: 4000px;
  border-bottom: 2px solid #122035;
  overflow: hidden;

}
</style>
