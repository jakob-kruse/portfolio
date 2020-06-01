<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();

    function scrollDown() {
        dispatch('scroll-click');
    }
</script>
<section class="section--top dyn-bg">
    <div class="name-container">
        <svg fill="none" viewBox="0 0 451 451" xmlns="http://www.w3.org/2000/svg" height="25%" width="25%"
             class="name-container__logo">
            <path d="m421.84 370.74c10.707 10.719 29.027 3.136 29.027-12.014v-265.73c0-15.15-18.32-22.733-29.027-12.014l-132.72 132.87c-6.63 6.638-6.63 17.391 0 24.028l132.72 132.87zm-54.958-340.87c10.7-10.712 3.113-29.014-12.027-29.014h-76.237c-9.389 0-17 7.6112-17 17v76.322c0 15.15 18.321 22.733 29.028 12.014l76.236-76.322zm-180.26-12.014c0-9.3888-7.611-17-17-17h-151.75c-9.3889 0-17 7.6112-17 17v208l6e-6 66c1e-6 9.389 7.6111 17 17 17h160.25c4.695 0 8.5-3.805 8.5-8.5v-282.5zm-168.75 366c-9.3889 0-17 7.612-17 17l-3e-6 33c-1e-6 9.389 7.6112 17 17 17h336.99c15.14 0 22.727-18.302 12.027-29.014l-83.544-83.637c-9.71-9.721-27.429-4.479-34.834 7.094-14.837 23.187-40.816 38.557-70.386 38.557h-160.25z"
                  clip-rule="evenodd" fill="#fff" fill-rule="evenodd"/>
        </svg>
        <div class="name-container__title">
            <h1 class="name-container__title--title">Jakob Kruse</h1>
            <h1 class="name-container__title--subtitle">Frontend Developer</h1>
        </div>
        <svg width="60" height="60" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"
             class="name-container__scroll" on:click={scrollDown}>
            <polygon points="10.5,16.08 5.63,10.66 6.37,10 10.5,14.58 14.63,10 15.37,10.66" fill="#fff"></polygon>
        </svg>
    </div>
</section>

<style>
    .section--top {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-content: center;
        scroll-snap-align: start;
        background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-2k.jpg");
        background-size: cover;
        background-blend-mode: darken;
    }

    .name-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
    }

    .name-container__title--title {
        text-align: center;
        color: white;
    }

    .name-container__title--subtitle {
        text-align: center;
        color: #AAAAAA;
    }

    .name-container__scroll {
        margin: 2rem;
        cursor: pointer;
    }

    /* Media Queries */

    /* Remove logo if the screen is very small */
    @media (max-width: 300px) {
        .name-container__logo {
            display: none;
        }
    }

    /* Extra small */
    @media (max-width: 600px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-2k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 48px;
        }

        .name-container__title--subtitle {
            font-size: 24px;
        }
    }

    /* Small */
    @media screen and (min-width: 601px) and (max-width: 960px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-2k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 92px;
        }

        .name-container__title--subtitle {
            font-size: 48px;
        }
    }

    /* Medium */
    @media screen and (min-width: 961px) and (max-width: 1264px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-2k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 92px;
        }

        .name-container__title--subtitle {
            font-size: 48px;
        }
    }

    /* Large */
    @media screen and (min-width: 1264px) and (max-width: 1904px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-2k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 92px;
        }

        .name-container__title--subtitle {
            font-size: 48px;;
        }
    }

    /* Extra Large */
    @media screen and (min-width: 1904px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-4k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 92px;
        }

        .name-container__title--subtitle {
            font-size: 48px;
        }
    }

    /* Very Large */
    @media screen and (min-width: 3000px) {
        .dyn-bg {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/bg-6k.jpg");
            background-size: cover;
        }

        .name-container__title--title {
            font-size: 92px;
        }

        .name-container__title--subtitle {
            font-size: 48px;
        }
    }
</style>