<script>
    export let imgSrc;
  </script>
  
  <style>
    .card {
      margin-top: 4rem;
      text-align: center;
      font-family: "Roboto Mono", sans-serif;
    }
  
    img {
      width: 100%;
    }

  </style>
  
  <div
    class="card"
    data-aos="fade-up"
    data-aos-once="true"
    data-aos-duration="1000">
      <img alt="author-avatar" data-src={imgSrc} class="lazyload" />
  </div>
  