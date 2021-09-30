<template>
    <div class="single-song">
        <div class="image">
          <img :src="songItem.poster" :alt="songItem.title">
        </div>
        <h3>{{ songItem.title }}</h3>
        <p>{{ songItem.author }}</p>
        <p>{{ songItem.date }}</p>
    </div>
</template>

<script>


export default {
    name: 'Song',
    props: ['songItem'],
}
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

.single-song{
  padding: 10px;
  background-color: $light-bg-color;
  color: $text-color;
  img{
      width: 100%;
  }
}

</style>