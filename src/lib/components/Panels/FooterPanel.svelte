<script lang="ts">
    import External from '../Links/External.svelte';
</script>

<section id="footer-panel" class="disable-padding">
    <section id="navigation">
        <nav id="navigation-links">
            <div class="group">
                <h2>General</h2>
                <a href="/">Frontpage</a>
                <a href="/blog">Blog</a>
            </div>
            <div class="group">
                <h2>Projects</h2>
                <a href="/projects">Projects</a>
            </div>
            <div class="group">
                <h2>Meta</h2>
                <a href="/credits">Credits</a>
                <a href="/attribution">Attribution</a>
            </div>
            <div class="group">
                <h2>Company</h2>
                <a href="/about">About</a>
                <a href="/contact">Contact Us</a>
                <a href="/brand">Brand</a>
            </div>
            <div class="group">
                <h2>Legal</h2>
                <a href="/legal">About</a>
                <a href="/legal/privacy">Privacy Policy</a>
                <a href="/legal/terms">Terms of Service</a>
            </div>
        </nav>
    </section>

    <section class="enable-spacing" id="bottom">
        <footer class="enable-spacing">
            <h1 class="logo">
                <span class="head">Lanza</span><span class="tail">forge</span>
            </h1>

            <p class="dim">
                © <b>Lanzaforge</b> 2026
            </p>

            <p>
                The official website of Lanzaforge, featuring our projects, documentation,
                showcases, and other creations.
            </p>
        </footer>

        <hr />

        <div id="footer" class="enable-spacing">
            <div id="connections">
                <External href="https://www.discord.com" showArrow={false} class="link">
                    <img src="/assets/socials/discord.svg" alt="Discord" />

                    <span class="handle">
                        @<span class="lanzaforge">lanzaforge</span>
                    </span>
                </External>

                <External
                    href="https://www.reddit.com/user/Lanzaforge/"
                    showArrow={false}
                    class="link"
                >
                    <img src="/assets/socials/reddit.svg" alt="Reddit" />

                    <span class="handle">
                        u/<span class="lanzaforge">Lanzaforge</span>
                    </span>
                </External>

                <External
                    href="https://bsky.app/profile/lanzaforge.bsky.social"
                    showArrow={false}
                    class="link"
                >
                    <img src="/assets/socials/bluesky.svg" alt="Bluesky" />

                    <span class="handle">
                        <span class="lanzaforge">lanzaforge</span>.bsky.social
                    </span>
                </External>

                <External href="https://x.com/lanzaforge" showArrow={false} class="link">
                    <img src="/assets/socials/x.svg" alt="X" />

                    <span class="handle">
                        @<span class="lanzaforge">lanzaforge</span>
                    </span>
                </External>

                <a href="mailto:mail@lanzoor.dev" class="link">
                    <img src="/assets/socials/email.svg" alt="Email" />

                    <span class="handle">
                        mail@<span class="lanzaforge">lanzaforge</span>.com
                    </span>
                </a>
            </div>
        </div>
    </section>
</section>

<style lang="css">
    :root {
        --footer-panel-bg: radial-gradient(circle at 50% -25%, #22054d 0%, #000 100%);
    }

    #footer-panel {
        padding: auto 10%;
        background: var(--footer-panel-bg);
        border-top: 3px solid rgba(133, 91, 224, 0.5);

        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        gap: 2%;
    }

    #footer-panel section {
        width: 100%;
    }

    #footer-panel #navigation {
        padding: 4em;
        border-bottom: 3px solid rgba(133, 91, 224, 0.5);
    }

    #footer-panel #navigation #navigation-links {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(10vw, 1fr));
        gap: 2em;
    }

    @media (max-width: 1200px) {
        #footer-panel #navigation #navigation-links {
            grid-template-columns: repeat(auto-fit, minmax(30vw, 1fr));
        }
    }

    #footer-panel #navigation #navigation-links .group {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 0.25em;
    }

    #footer-panel #navigation #navigation-links .group h2 {
        margin: 0.25em 0 0.5em 0;
        font-size: 1.1em;
        color: rgb(123, 61, 255);
    }

    #footer-panel #navigation #navigation-links .group a {
        color: rgba(255, 255, 255, 0.7);
    }

    #footer-panel #navigation #navigation-links .group a:hover {
        color: white;
    }

    #footer-panel #connections {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        column-gap: 1.5em;
        row-gap: 0.5em;

        margin: 0 2em;
    }

    :global(#footer-panel #connections a:not(.plain):has(> img)) {
        opacity: 0.75;
        transition: opacity 500ms ease;
    }

    :global(#footer-panel #connections a:not(.plain):has(> img):hover) {
        opacity: 1;
        text-decoration: none;
    }

    #footer-panel #connections .handle {
        color: rgb(110, 55, 192);
    }

    #footer-panel #connections .handle .lanzaforge {
        color: rgb(188, 143, 255);
    }

    @media (max-width: 768px) {
        :global(#footer-panel #connections a > img) {
            width: 2em;
            height: 2em;
        }

        #footer-panel #connections {
            justify-content: flex-start;
            column-gap: 1em;
            row-gap: 0.25em;

            margin: 0;
        }

        #footer-panel #connections .handle {
            display: none;
        }
    }
</style>
