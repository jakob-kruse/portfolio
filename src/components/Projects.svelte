<script>
    const projects = [
        {
            name: "Placeholder",
            icon: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.freebiesupply.com%2Flogos%2Flarge%2F2x%2Fstarbucks-coffee-logo-black-and-white.png&f=1&nofb=1',
            href: ''
        }, {
            name: "Placeholder",
            icon: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.freebiesupply.com%2Flogos%2Flarge%2F2x%2Fstarbucks-coffee-logo-black-and-white.png&f=1&nofb=1',
            href: ''
        }, {
            name: "Placeholder",
            icon: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.freebiesupply.com%2Flogos%2Flarge%2F2x%2Fstarbucks-coffee-logo-black-and-white.png&f=1&nofb=1',
            href: ''
        },
    ]
</script>

<div class="projects-container">
    {#if projects.length > 0}
        {#each projects as project}
            <a href="{project.href || '#'}">
                <div class="projects-container__item">
                    <img src="{project.icon}" alt="{project.name}" class="projects-container__item__icon">
                    <span class="projects-container__item__name">{ project.name }</span>
                </div>
            </a>
        {/each}
    {:else}
        <p class="projects-container__fallback">No Projects yet :(</p>
    {/if}
</div>

<style>
    .projects-container {
        display: flex;
        flex-wrap: wrap;
        align-content: center;
        justify-content: flex-end;
        width: 100%;
    }

    @media screen and (max-width: 1264px) {
        .projects-container {
            justify-content: center;
        }
    }

    .projects-container__item {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 150px;
        max-height: 150px;
        margin: 10px;
        padding: 20px;
        background-color: white;
        transition: background-color .5s;
        cursor: pointer;
    }

    .projects-container__item:hover {
        background-color: #212121;
        border: 1px solid white;
        transform: scale(1.05);
        transition: transform 0.25s;
    }

    .projects-container__item:hover > .projects-container__item__name {
        color: white
    }

    .projects-container__item:hover > .projects-container__item__icon {
        color: white;
        padding: 0px;
    }

    .projects-container__item__icon {
        transition: padding .5s;
        padding: 5px;
    }

    .projects-container__item__name {
        transition: color .5s;
        color: black;
        font-weight: bold;
    }
</style>