<script>
    import { onMount } from 'svelte';
    import SectionTop from '../components/SectionTop.svelte'
    import SectionBottom from "../components/SectionBottom.svelte";

    onMount(async () => {
        const ackeeTracker = (await import('ackee-tracker')).default;

        ackeeTracker.create({
            server: 'https://ackee.lastdigitsofpi.dev',
            domainId: '5eea4c0f-e468-47eb-8b18-c3ec9f292bc4'
        }).record()
    });

    function scrollDown() {
        document.getElementsByClassName("section--bottom")[0].scrollIntoView({behavior: "smooth"});
    }
</script>

<SectionTop on:scroll-click={scrollDown}/>
<SectionBottom/>
