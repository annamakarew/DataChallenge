<script>
  let { title, subtitle } = $props();
</script>

<div class="title-card">
  <div class="content">
    <h1>{title}</h1>
    <p>{subtitle}</p>
  </div>
</div>

<style>
  .title-card {
    background-color: #1f2d3d;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    box-sizing: border-box;
    font-family: "Inter", sans-serif;
  }

  .content {
    max-width: 850px;
    background-color: #253847;
    padding: 2rem;
    border: 6px solid #d4af37;
    border-radius: 2rem;
    box-shadow: 16px 16px #3c5a72;
  }

  h1 {
    font-size: 3rem;
    margin: 0;
    color: #f0f4f8;
    text-shadow: 1px 1px 0 #1f2d3d;
  }

  p {
    font-size: 1.3rem;
    color: #dde2e6;
    margin-top: 1rem;
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }

    p {
      font-size: 1.1rem;
    }
  }
</style>
