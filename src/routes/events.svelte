<svelte:head>
    <title>Events</title>
</svelte:head>

<script>
    import {onMount} from 'svelte';
    import EventCards from '../components/EventCards.svelte';
    import AOS from 'aos';
    import 'aos/dist/aos.css';
    import 'aos/dist/aos.js';
    import 'lazysizes';
    import 'lazysizes/plugins/parent-fit/ls.parent-fit';

    let datas = [];

    onMount(async () => {
        AOS.init()
        const res = await fetch('./Data/events.json');
        const textData = await res.text();
        datas = await JSON.parse(textData);
    });

    const compareDate = (prevTime) => {
        let [prevDate,prevMonth,prevYear] = prevTime.split("-");
        let [month, date, year]    = ( new Date() ).toLocaleDateString().split("/");
        if(+prevDate < +date || +prevMonth < +month || +prevYear < +year) {
            return false;
        } else {
            return true;
        }
    }
</script>


<div class="main-title">EVENTS</div>
<div class="sub-title"> Upcoming Events</div>
{#each datas as data (data.id)} 
    {#if compareDate(data.formatDate)}
        <EventCards title={data.title} time={data.time}
    location={data.location} imagelink={data.imagelink} />
    {/if}
{/each}
{#each datas as data (data.id)} 
    {#if !compareDate(data.formatDate)}
        <EventCards title={data.title} time={data.time}
    location={data.location} imagelink={data.imagelink} name={data.name} company={data.company}/>
    {/if}
{/each}

<style>
    .main-title {
        font-size: 3rem;
        font-weight: bold;
        color: #f74700;
    }

    .sub-title {
        font-size: 2rem;
        margin-top: 4rem;
        color: #f74700;
    }

    @media (max-width:700px) {
        .main-title {
            font-size: 2rem;
            color: #f74700;
        }
    }
</style>