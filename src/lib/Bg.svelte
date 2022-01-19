<script lang="ts">
    import bg from '../../static/bg.svg';
</script>

<img id="header-image" src={bg} alt="sunrise">

<style lang="scss">
  img {
    position: fixed;
    object-fit: cover;
    object-position: center;
    height: 100%;
    width: 100%;
    z-index: -1;
  }
</style>
