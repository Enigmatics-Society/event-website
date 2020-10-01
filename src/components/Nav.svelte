<script>
	let active = false;
  let addActive = "";

  let isOpen = false;

  function handleClick() {
    isOpen = !isOpen;
  }
</script>

<style>
	.nav-head {
    max-height: 90px;
    width: auto;
  }
  nav {
    font-weight: 300;
    padding: 1em 2em;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 10vh;
  }
	ul {
    margin: 0;
    padding: 0;
    display: flex;
  }

  li {
    list-style: none;
  }

  li:not(:last-child) {
    margin-right: 50px;
  }

  .nav-link {
    text-decoration: none;
    padding: 0.1em 0.25em;
    display: block;
    text-transform: uppercase;
    font-size: 1.6rem;
    transition: all 0.5s;
    position: relative;
    border-bottom: 2px solid #000;
  }

  .nav-link::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    z-index: -1;
    height: 0;
    opacity: 0;
    transition: all 0.6s;
    background-color: #df85d9;
  }

  .nav-link:hover::after {
    height: 100%;
    opacity: 1;
  }

  .nav-link:hover {
    color: #fff;
	border-bottom: 2px solid #70314f;
  }

  .burger-container {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    cursor: pointer;
    transition: all 0.5s ease-in-out;
    display: none;
    z-index: 10;
  }

  .hamburger-icon {
    width: 30px;
    height: 2px;
    background: #000;
    border-radius: 5px;
    transition: all 0.5s ease-in-out;
  }

  .hamburger-icon::before,
  .hamburger-icon::after {
    content: "";
    position: absolute;
    width: 30px;
    height: 2px;
    background: #000;
    border-radius: 5px;
    transition: all 0.5s ease-in-out;
  }

  .hamburger-icon::before {
    transform: translateY(-11px);
  }

  .hamburger-icon::after {
    transform: translateY(11px);
  }

  .burger-container.open .hamburger-icon {
    transform: translateX(-50px);
    background: transparent;
  }

  .burger-container.open .hamburger-icon::before {
    transform: rotate(45deg) translate(35px, -35px);
  }

  .burger-container.open .hamburger-icon::after {
    transform: rotate(-45deg) translate(35px, 35px);
  }

  .nav-overlay {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background: #000;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;
    transform: translateX(100%);
    transition: all 0.6s ease-in-out;
    z-index: 5;
  }

  .logo-container:hover .logo-back{
    transform: rotateX(0deg);
  }

  .nav-overlay.open {
    transform: translateX(0%);
  }

  .nav-overlay-list {
    position: relative;
    display: flex;
    flex-direction: column;
    width: 100vw;
  }

  .nav-overlay-list li {
    position: relative;
    list-style: none;
    text-align: center;
    display: block;
  }

  .nav-overlay-list li a {
    position: relative;
    text-decoration: none;
    font-size: 1.4em;
    padding: 0 10px;
    color: #000;
    font-weight: 700;
    text-transform: uppercase;
    display: inline-block;
    margin-top: 40px;
    border: none;
    margin-bottom: 30px;
  }

  .divider-big {
    height: 1px;
    width: 70%;
    margin: 0 auto;
  }
	@media (max-width: 768px) {
    .nav-links {
      display: none;
    }

    .nav-head {
      max-height: 70px;
    }

    li:not(:last-child) {
      margin-right: 0;
      margin-bottom: 1em;
    }

    .burger-container {
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
    }
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
    .logo-back{
      display: none;
    }
    .logo-container:hover .logo-front{
      transform: none;
    }
  }

  .logo-container {
    text-align: center;
    width: 90px;
    height: 90px;
    font-size: 2rem;
    position: relative;
    transform-style: preserve-3d;
    transition: .4s;
    perspective: 90px;
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
  .logo-back{
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
  .logo-back > p{
    line-height: 1.9;
    word-spacing: 1.5;
  }
  .logo-back > h2{
    background-image: linear-gradient(to right,#ffc7d1, #5a03cc);
    -webkit-background-clip: text;
    color: transparent;
    font-weight: 700;
    margin: 5px;
  }  
</style>

<nav>
	<div class = "logo-container">
		<div class="logo-front">
		<a href=".">
			<img src = "Icon.png" alt="header" class="nav-head" />
		</a>
		</div>
		<div class="logo-back">
			<a href = ".">
				<img src = "iiit.png" alt="header1" class="nav-head"/>
			</a>
		</div>
		<div class="burger-container" on:click={handleClick} class:open={isOpen}>
			<div class="hamburger-icon"></div>
		</div>
	</div>
	<ul class="nav-links ">
		<li><a class="nav-link" href=".">home</a></li>
		<li><a class="nav-link" href="events">events</a></li>
		<li><a rel="prefetch" class="nav-link" href="team">team</a></li>
	  </ul>
	  <div class="nav-overlay" on:click={handleClick} class:open={isOpen}>
	  </div>
</nav>
