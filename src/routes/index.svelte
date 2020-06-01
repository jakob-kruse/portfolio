<script>
    import SectionTop from '../components/SectionTop.svelte'
    import SectionBottom from "../components/SectionBottom.svelte";

    function scrollDown() {
        document.getElementsByClassName("section--bottom")[0].scrollIntoView({behavior: "smooth"});
    }
</script>

<SectionTop on:scroll-click={scrollDown}/>
<SectionBottom/>
