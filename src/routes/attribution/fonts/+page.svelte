<script lang="ts">
    import { onMount } from 'svelte';

    const fonts = [
        {
            internalName: 'jetbrains-mono',
            name: 'JetBrains Mono',
        },
        {
            internalName: 'fira-code',
            name: 'Fira Code',
        },
        {
            internalName: 'noto-sans',
            name: 'Noto Sans',
        },
        {
            internalName: 'noto-sans-mono',
            name: 'Noto Sans Mono',
        },
    ];

    let activeFont = $state(fonts[0]);

    onMount(() => {
        const observer = new IntersectionObserver(
            (entries) => {
                for (const entry of entries) {
                    if (!entry.isIntersecting) continue;

                    const font = fonts.find((f) => f.internalName === entry.target.id);

                    if (font) {
                        activeFont = font;
                    }
                }
            },
            {
                threshold: 0.6,
            }
        );

        document.querySelectorAll('.font').forEach((el) => observer.observe(el));

        return () => observer.disconnect();
    });

    let animate = $state(false);

    $effect(() => {
        activeFont;

        animate = false;

        requestAnimationFrame(() => {
            animate = true;
        });
    });
</script>

<svelte:head>
    <title>Font Credits | lanzoor.dev</title>
</svelte:head>

<section class="stretched" id="intro">
    <h1>Fonts</h1>

    <blockquote class="dim">
        <b>typography</b> <span class="ipa">/taɪˈpɑːgrəfi/</span>
        <span class="dimmer">(noun)</span>:<br />
        the art and technique of printing with movable type.
    </blockquote>

    <p>
        <b>Fonts make a website truly unique and distinct.</b><br />
        They define <b>the vibe and personality</b> of a website, turning simple text into something
        memorable.<br />
        <b>Lanzaforge's projects use multiple fonts, each chosen for its appropriate context.</b>
    </p>

    <p>
        <b
            >This page contains all of the fonts used across Lanzaforge's projects, as well as their
            attribution links.</b
        >
    </p>

    <div class="down-arrow">Keep scrolling</div>
</section>

<section id="showcase">
    <div id="font-showcase" class={activeFont.internalName} class:animate>
        <h1>{activeFont.name}</h1>

        <p>
            The quick brown fox jumps over the lazy dogs.<br /><br />
            ABCDEFGHIJKLMNOPQRSTUVWXYZ<br />
            abcdefghijklmnopqrstuvwxyz<br />
        </p>
    </div>

    <div id="font-description">
        <div class="font jetbrains-mono" id="jetbrains-mono">
            <h1>JetBrains Mono</h1>

            blah blah blah
        </div>

        <div class="font fira-code" id="fira-code">
            <h1>Fira Code</h1>

            blah blah blah
        </div>

        <div class="font noto-sans" id="noto-sans">
            <h1>Noto Sans</h1>

            notorious
        </div>

        <div class="font noto-sans-mono" id="noto-sans-mono">
            <h1>Noto Sans Mono</h1>

            does mono stand for monokuma
        </div>
    </div>
</section>

<style lang="css">
    #font-showcase {
        display: none;
    }
    @media (min-width: 1080px) {
        #showcase {
            display: flex;
            flex-direction: row;
            gap: 4rem;
            align-items: flex-start;

            overflow: visible;
        }

        #font-showcase {
            position: sticky;
            top: 0;

            width: 40vw;
            height: 100vh;

            display: flex;
            flex-direction: column;

            justify-content: center;
            align-items: flex-start;

            padding: 2rem;
        }

        #font-showcase.animate {
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        #font-description {
            width: 100vh;
        }

        .font {
            min-height: 100vh;
            width: 100%;

            display: flex;
            flex-direction: column;
            gap: 2em;
            justify-content: center;
        }
    }
</style>
