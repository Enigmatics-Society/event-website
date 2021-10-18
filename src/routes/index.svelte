<script>
  let bgImage = 'https://hacktoberfest.digitalocean.com/_nuxt/img/logo-hacktoberfest-full.f42e3b1.svg';
</script>

<style>
  div {
    text-align: center;
  }
  img{
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;

  }

  h1{
    color:rgb(53, 34, 26);
    font-weight: bolder;
  }
  p{
    color:rgba(145,168,140,var(--tw-text-opacity));
  }
  a{
    text-decoration: none;
    color:rgb(255, 255, 255);
  }
  .justify-center {
      justify-content: center;
  }
  .items-center {
      align-items: center;
  }
  .flex {
      display: flex;
  }
  .font-bold {
      font-weight: 700;
  }
  .text-lgreen {
      --tw-text-opacity: 1;
      color: rgba(145,168,140,var(--tw-text-opacity));
  }
  .pb-2 {
      padding-bottom: .5rem;
  }
  .text-xs {
      font-size: .75rem;
      line-height: 1rem;
  }
  .md\:text-base {
      font-size: 1rem;
      line-height: 1.5rem;
  }
  h4 {
      display: block;
      margin-block-start: 1.33em;
      margin-block-end: 1.33em;
      margin-inline-start: 0px;
      margin-inline-end: 0px;
      font-weight: bold;
      text-align: center;

  }
  .card {
    box-shadow: 0 4px 8px 0 rgba(255, 132, 50, 0.568);
    transition: 1s;
    width: auto;
    border-radius: 20px;
  }
  .card:hover .container{
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    transform: rotateY(180deg);
  }
  .container {
    position: relative;
    transition: all 0.75s ease;
    transform-style: preserve-3d;
  }
  .card-front{
    box-shadow: 0 4px 8px 0 rgba(255, 132, 50, 0.568);
    border-radius: 20px;
    padding:3% 3%;
    margin: auto;
  }
  .card-front, .card-back {
    position: absolute;
    width: auto;
    height: auto;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
  }
  .card-back {
    background-color: #f74700;
    border-radius: 20px;
    padding:3% 3%; 
    transform: rotateY(180deg);
    margin: auto;
  }
</style>
<br>
<div class="card">
  <div class="container">
    <div class="card-front">
      <div>
        <img src="{bgImage}" alt="">
      </div>
      <h4 class="font-bold text-lgreen pb-2 text-xs md:text-base pt-5">Presented by</h4>
      <div class="flex space-x-3 md:space-x-10 justify-center items-center">
        <a target="_blank" rel="noopener" href="https://www.digitalocean.com">
          <img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-digitalocean-gr.f6faef2.svg" alt="DigitalOcean logo" class="h-6 md:h-12">
        </a> 
        <a target="_blank" rel="noopener" href="https://hacktoberfest.appwrite.io/">
          <img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-appwrite-gr.1161116.svg" alt="Appwrite logo" class="h-6 md:h-12">
        </a> 
        <a target="_blank" rel="noopener" href="http://devmesh.intel.com/">
          <img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-intel-gr.a510816.svg" alt="Intel logo" class="h-5 md:h-10">
        </a>
        <a target="_blank" rel="noopener" href="https://deepsource.io/hacktoberfest/">
          <img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-deepsource-gr.37aa9bc.svg" alt="Deepsource logo" class="h-6 md:h-12">
        </a>
      </div>
    </div>
    <div class="card-back">
      <h1> About </h1>
      <br>
      <p>
        Welcome to the HacktoberFest event organised by IIIT Sonepat.
        <br>
        As our society grows more and more dependent on computers, the ownership of the software we run needs to be more and more decentralised and open sourced.
        <br>
        Whether you are a big contributor or a first time programmer, you are welcome to join this event. Learning some and sharing some is key.
        <br>
        From getting started with open source to making your first PR, we will be covering it all.
        <br>
        A special thanks to Digital Ocean for their immense support</p>	
         <br>
        <p><a href = "##"> Youtube Live Link </a></p>
    </div>
  </div>
</div>

