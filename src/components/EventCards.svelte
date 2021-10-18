<script>
  export let title;

  export let time;
  export let location;
  export let imagelink;
  export let name;
  export let company;
  import Icon from "svelte-awesome/components/Icon.svelte";
  import { calendar, mapMarker } from "svelte-awesome/icons";
</script>

<style>
  .event-container {
    font-family: "Red Hat Display", sans-serif;
    display: flex;
    margin-top: 3rem;
    padding-bottom: 3rem;
    border-bottom: 1px solid white;
  }

  .right {
    padding: 0 0 0 2rem;
    font-weight: 100;
  }

  .left {
    max-width: 320px;
    height: auto;
  }

  .left img {
    width: 100%;
    height: auto;
  }

  .title {
    font-size: 2rem;
    font-weight: bold;
  }

  @media (max-width: 700px) {
    .event-container {
      flex-direction: column;
      font-size: 1rem;
    }

    img {
      height: auto;
      width: 100%;
    }

    .title {
      font-size: 1.5rem;
    }

    .right {
      padding: 1rem 0 0 0;
    }
  }
  p{
    color: rgb(216, 136, 104);
  }

  h2{
      color: #f74700;
      text-align: center;
    }
  h4{
      color: rgb(248, 129, 82);
      text-align: center;
    }
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

  
    img {
      width: 100%;
      height:140px;
      border-radius: 30px;
      object-fit:cover;
    }
    
    .container {
      padding: 20px 16px;
    }
</style>

<div
  class="event-container"
  data-aos="fade-up"
  data-aos-once="true"
  data-aos-duration="1000">
  <div class="left card">
    <img alt="event poster" data-src={imagelink} class="lazyload" />
    <div class="container">
      <h2><b>{name}</b></h2>
      <h4>{company}</h4>
    </div>
  </div>
  <div class="right">
    <h2 class="title">{title}</h2>
    <br />
    <p class="location">
      &nbsp;
      <Icon
        data={mapMarker}
        style="vertical-align: sub;"
        scale="1.4" /><span>&nbsp;&nbsp;
        {location}<span>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <Icon
            data={calendar}
            style="vertical-align: sub;"
            scale="1.4" /><span> &nbsp; {time}</span></span></span>
    </p>
  </div>
</div>
