<script>
  import Index from "./index.svelte";
</script>

<svelte:head>
  <title>About</title>
</svelte:head>

<div class="main-title">ABOUT US</div>
<div class="sub-title"><u>IIIT SONEPAT</u></div>
<div class="card">
  <img alt="colleg-image" src="college.png" class="main-image" />
</div>
<p class="main-content">
  <b>Indian Institute of Information Technology, Sonepat (IIIT, Sonepat)</b> is one
  of the Indian Institutes of Information Technology located at Sonepat, Haryana.
  Established in the year 2014-15, by an Act of Parliament the Indian Institute of
  Information Technology Sonepat is an Institute of National Importance created by
  the MHRD, Government of India in the Public Private Partnership model.
</p>

<style>
  .main-title {
    font-size: 3rem;
    font-weight: bold;
    text-align: center;
    padding-bottom: 1rem;
    border-bottom: 2px solid rgb(255, 168, 133);
    color: #f74700;
  }
  .main-content {
    font-size: 1.5rem;
    font-weight: 400;
    text-align: center;
    padding-bottom: 1rem;
    border-bottom: 2px solid rgb(255, 168, 133);
    color: #f74700;
  }
  .main-image {
    display: block;
    margin-right: auto;
    margin-left: auto;
    width: 100%;
    border-radius: 30px;
    box-shadow: 0 4px 8px 0 rgba(247, 70, 0, 0.205);
    transition: 0.3s;
  }
  .card {
    margin: auto;
    width: 60%;
    border-radius: 30px;
  }
  .main-image:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
  }
  .sub-title {
    font-size: 1.8rem;
    margin-top: 1rem;
    margin-bottom: 1rem;
    color: #f74700;
    text-align: center;
    font-weight: bold;
  }
</style>
