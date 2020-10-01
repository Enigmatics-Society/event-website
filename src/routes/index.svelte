<style>

.logo-container {
    text-align: center;
    width: 850px;
    height: 400px;
    font-size: 2rem;
    position: relative;
    transform-style: preserve-3d;
    transition: .4s;
    perspective: 800px;
  }
  .logo-front{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    transform: rotateX(0deg);
    transition: .4s;
  }
  .logo-container:hover .logo-front{
    transform: rotateX(-180deg);
  }
  .about-back{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    font-size: 1.1rem;
    backface-visibility: hidden;
    transform: rotateX(180deg);
    transition: .4s;
  }
  .about-back > p{
    line-height: 1.9;
    word-spacing: 1.5;
  }
  .about-back > h2{
    background-image: linear-gradient(to right,#ffc7d1, #5a03cc);
    -webkit-background-clip: text;
    color: transparent;
    font-weight: 700;
    margin: 5px;
  }  
  .divider{
    height: 3px;
    width: 140px;
    background-image: linear-gradient(to right, #ffc7d1, #5a03cc);
    position: absolute;
    left: 50%;
    transform: translate(-50%, -30%);
  }
  .logo-container:hover .about-back{
    transform: rotateX(0deg);
  }
	  img {
    width: 100%;
    max-width: 600px;
    margin: 0 0 1em 0;
  }
  a {
    outline: none;
  }

.logo-front {
      font-size: 1.5rem;
    }
  @media (max-width: 500px) {
    .logo-container {
      display: inline-block;
      width: 300px;
      height: 160px;
      left: 50%;
      transform: translateX(-50%);
    }
    .logo-front > p{
      font-size: 1.1rem;
    }
    .about-back{
      display: none;
    }
    .logo-container:hover .logo-front{
      transform: none;
    }
    #social {
      
      margin-top: 110px;
    }
  }
</style>

<svelte:head>
	<title>IIIT Sonepat Hacktober Fest Meetup</title>
</svelte:head>

<div class="logo-container">
	<div class="logo-front">
		<img alt="logo" src="logo.png" >
	</div>
	<div class="about-back">
		<h2> About </h2>
		<div class="divider"></div>
		<p>Test</p>	
	</div>
</div>

