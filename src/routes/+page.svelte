<section id="intro" class="disable-initial-padding">
    <header class="enable-initial-padding">
        <div class="headings">
            <h2 class="welcome">
                Welcome to <span class="logo"
                    ><span class="head">Lanza</span><span class="tail">forge</span></span
                >
            </h2>

            <h1>Building things worth using.</h1>
        </div>

        <div class="description">
            <p>
                <b>Lanzaforge is a place for building things.</b>
            </p>

            <p>
                We create software, websites, tools, and experiments that we're interested in. Some
                projects are practical, some are experimental, and some exist simply because we
                wanted to see if we could make them.
            </p>
        </div>

        <a class="plain" href="/projects">
            <button>Explore projects ></button>
        </a>
    </header>
</section>

<style lang="css">
    #intro header {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 2em;

        text-align: center;
        background: radial-gradient(circle at 50% 50%, rgba(100, 0, 255, 0.2), transparent);
        min-height: 100vh;
    }

    #intro header .headings {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #intro header .headings h1 {
        font-size: 4em;
        color: rgb(141, 66, 255);
        text-shadow: 0 0 2em rgba(164, 103, 255, 0.25);
    }

    #intro .headings .welcome {
        font-size: 1.25em;
        font-weight: 400;

        padding: 0.25em 1em;

        border: 2px solid rgba(100, 0, 255, 0.2);
        border-radius: 2147483647px;
        background: rgba(100, 0, 255, 0.1);
    }

    #intro header .description {
        font-size: 1.25em;
        opacity: 0.8;
        max-width: 80%;
    }

    #intro header button {
        color: black;
        font-size: 1.25em;

        padding: 0.5em 1em;

        background: rgb(164, 103, 255);
        border: 2px solid rgb(164, 103, 255);
        border-radius: 2147483647px;
        box-shadow: 0 0 1em rgba(164, 103, 255, 0.5);

        transition: 200ms ease;
    }

    #intro header button:hover {
        color: rgb(164, 103, 255);
        text-shadow: 0 0 1em rgba(164, 103, 255, 0.5);
        letter-spacing: 0.05em;

        background: rgb(164, 103, 255, 0.1);
        box-shadow:
            0 0 1em rgba(164, 103, 255, 0.25),
            inset 0 0 1em rgba(164, 103, 255, 0.25);
    }
</style>
