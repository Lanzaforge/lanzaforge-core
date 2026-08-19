<script lang="ts">
    import External from '$lib/components/Links/External.svelte';
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

<section id="intro">
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

            <p>
                Links:
                <External href="https://www.jetbrains.com/lp/mono/">Website</External> |
                <External href="https://fonts.google.com/specimen/JetBrains+Mono"
                    >Google Fonts</External
                > |
                <External href="https://github.com/JetBrains/JetBrainsMono">GitHub</External>
            </p>

            <p>Designer(s):</p>
            <ul>
                <li>
                    <b>JetBrains</b><br />
                    Links:
                    <External href="https://www.jetbrains.com/">Website</External> |
                    <External href="https://github.com/JetBrains">GitHub</External>
                </li>
            </ul>

            <p>
                License: <External
                    href="https://github.com/JetBrains/JetBrainsMono/blob/master/OFL.txt"
                    >SIL Open Font License 1.1</External
                >
            </p>

            <p>
                Identifier: <code>jetbrains-mono</code>
            </p>

            <p>Usage: Used for code, technical information, and other monospaced text.</p>
        </div>

        <div class="font fira-code" id="fira-code">
            <h1>Fira Code</h1>

            <p>
                Links:
                <External href="https://github.com/tonsky/FiraCode">Github</External> |
                <External href="https://fonts.google.com/specimen/Fira+Code">Google Fonts</External>
            </p>

            <p>Designer(s):</p>
            <ul>
                <li>
                    <b>tonsky</b><br />
                    Links:
                    <External href="https://github.com/tonsky">GitHub</External> |
                    <External href="https://tonsky.me/">Website</External><br />
                </li>
            </ul>

            <p>
                License: <External
                    href="https://github.com/tonsky/FiraCode/blob/master/LICENSE     "
                    >SIL Open Font License 1.1</External
                >
            </p>

            <p>
                Identifier: <code>fira-code</code>
            </p>

            <p>Usage: Used for code, technical information, and other monospaced text.</p>
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
    #showcase {
        display: flex;
        flex-direction: row;
        gap: 4rem;
        align-items: flex-start;

        overflow: visible;

        background: radial-gradient(circle at bottom center, rgba(100, 0, 255, 0.25), transparent),
            black;
        background-position: center center;
        background-attachment: fixed;
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

        padding: 2em;
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
        gap: 0.5em;
        justify-content: center;
    }

    @media (max-width: 1080px) {
        #font-showcase {
            display: none;
        }
    }
</style>
