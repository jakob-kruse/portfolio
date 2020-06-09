<script>
    import { onMount } from 'svelte';
    import SectionTop from '../components/SectionTop.svelte'
    import SectionBottom from "../components/SectionBottom.svelte";

    onMount(async () => {
        const ackeeTracker = (await import('ackee-tracker')).default;

        ackeeTracker.create({
            server: 'https://ackee.lastdigitsofpi.dev',
            domainId: '813c633b-cd8b-4b28-8e26-e73d16afab2d'
        }).record()
    });

    function scrollDown() {
        document.getElementsByClassName("section--bottom")[0].scrollIntoView({behavior: "smooth"});
    }
</script>

<SectionTop on:scroll-click={scrollDown}/>
<SectionBottom/>
