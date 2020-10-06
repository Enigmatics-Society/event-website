<svelte:head>
  <title>Leadership</title>
</svelte:head>


<script>
  import {onMount} from 'svelte';
  import TeamComponent from '../components/TeamComponent.svelte';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import 'aos/dist/aos.js';
  import 'lazysizes';
  import 'lazysizes/plugins/parent-fit/ls.parent-fit';

  let datas = [];

  onMount(async () => {
    AOS.init();
    const res = await fetch('./Data/faculty.json');
    const textData = await res.text();
    datas = await JSON.parse(textData);
  });
</script>

<section class="card-list">
  {#each datas as data (data.id)} 
    <TeamComponent imgSrc={data.imgSrc}/>
  {/each}
</section>

<style>
  .main-title {
    font-size: 3rem;
    font-weight: bold;
    text-align: center;
    padding-bottom: 1rem;
    border-bottom: 2px solid #ffc7d1;
  }

  .card-list {
    display:grid;
    grid-template-columns: repeat(2,1fr);
    gap:7rem 3rem;
  }

  
  @media (max-width:700px) {
    .main-title {
      font-size:2.5rem;
    }
    .card-list {
      grid-template-columns: 1fr;
      gap:2rem 1rem;
    }
  }
</style>
