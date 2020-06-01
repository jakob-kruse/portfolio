<script>
    import Projects from "./Projects.svelte";
</script>
<section class="section--bottom">
    <div class="section--bottom__about-title">
        <h1>ABOUT ME</h1>
    </div>

    <div class="section--bottom__about-content">
        <p>I'm a web developer living in North Rhine-Westphalia, Germany. I started programming around 6 years ago, with
            simple HTML Websites in school. Then I went through some Python and C# phases and now, at 18 years old, I'm
            back at web development again. But it's not just simple HTML anymore, nowadays I use JavaScript frameworks
            like Vue.js and Svelte to realize my projects!</p>
        <div class="section--bottom__about-content__social-media">

        </div>
    </div>

    <div class="section--bottom__projects-title">
        <h1>PROJECTS</h1>
    </div>

    <div class="section--bottom__projects-content">
        <Projects/>
    </div>
</section>

<style>
    .section--bottom {
        min-height: 100vh;
        justify-content: center;
        align-content: center;
        scroll-snap-align: start;
        background-color: #212121;

        padding: 48px;

        display: grid;
        grid-template-columns: 2fr 1fr;
        grid-template-rows: 1fr 8fr;
        grid-column-gap: 100px;
        grid-template-areas: "about-tite projects-title" "about-content projects-content";
    }

    .section--bottom__about-title {
        grid-column: 1;
        grid-row: 1;
    }

    .section--bottom__about-title > h1 {
        font-size: 128px;
        color: #AAAAAA;
    }

    .section--bottom__about-content {
        grid-column: 1;
        grid-row: 2;
    }

    .section--bottom__about-content > p {
        font-size: 24px;
        line-height: 1.8;
        color: #AAAAAA;
    }

    .section--bottom__projects-title {
        grid-column: 2;
        grid-row: 1;
    }

    .section--bottom__projects-title > h1 {
        font-size: 128px;
        text-align: end;
        color: #AAAAAA;
    }

    .section--bottom__projects-content {
        grid-column: 2;
        grid-row: 2;
    }



    @media screen and (max-width: 1264px) {
        .section--bottom {
            padding: 48px;

            display: grid;
            grid-template-columns: 1fr;
            grid-template-rows: 1fr auto 1fr auto;
            grid-column-gap: 100px;
            grid-template-areas: none;
        }

        .section--bottom__about-title > h1 {
            font-size: 48px;
        }

        .section--bottom {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr auto 1fr auto;
        }

        .section--bottom__about-title {
            grid-column: 1;
            grid-row: 1;
        }

        .section--bottom__about-content {
            grid-column: 1;
            grid-row: 2;
        }

        .section--bottom__about-content > p {
            font-size: 18px;
            line-height: 1.4;
            text-align: center;
            color: #AAAAAA;
        }

        .section--bottom__projects-title {
            grid-column: 1;
            grid-row: 3;
        }

        .section--bottom__projects-title > h1 {
            font-size: 48px;
            text-align: center;
            color: #AAAAAA;
        }

        .section--bottom__projects-content {
            grid-column: 1;
            grid-row: 4;
        }
    }
</style>