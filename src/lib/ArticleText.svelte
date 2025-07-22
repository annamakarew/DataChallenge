<script>
  let { children } = $props();
</script>

<div class="article-text">
  <p>
    {@render children()}
  </p>
</div>

<style>
  .article-text {
    margin: 50vh auto;
    width: 70%;
    background-color: #ffffff; /* clean white background for readability */
    color: #1f2d3d; /* deep slate/navy text */
    border: solid #d4af37 3px; /* muted gold for continuity with title card */
    border-radius: 20px;
    padding: 20px;
    box-shadow: 8px 8px 16px rgba(31, 45, 61, 0.2); /* soft navy-toned shadow */
    font-size: 25px;
  }
</style>
