<script>
  export let imgSrc;
  export let name;
  export let role;
</script>

<style>
  .card {
    margin: auto;
    box-shadow: 0 4px 8px 0 rgba(247, 70, 0, 0.205);
    transition: 0.3s;
    width: 60%;
    border-radius: 30px;
  }
  .card:hover {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
  }

  .container {
    padding: 20px 16px;
  }

  img {
    width: 100%;
    border-radius: 30px;
  }
  h2{
    color: #f74700;
    text-align: center;
  }
  h4{
    color: rgb(255, 255, 255);
    text-align: center;
  }

</style>


<div class="card"
data-aos="fade-up"
  data-aos-once="true"
  data-aos-duration="1000">
  <img alt="author-avatar" data-src={imgSrc} class="lazyload">
  <div class="container">
    <h2><b>{name}</b></h2>
    <h4><b>{role}</b></h4>
  </div>
</div>
