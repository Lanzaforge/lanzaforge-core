<script lang="ts">
    import External from '$lib/components/Links/External.svelte';
    import { onMount } from 'svelte';
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

            <p>Creator<span class="dim">(s)</span>:</p>
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
                <External href="https://github.com/tonsky/FiraCode">GitHub</External> |
                <External href="https://fonts.google.com/specimen/Fira+Code">Google Fonts</External>
            </p>

            <p>Creator<span class="dim">(s)</span>:</p>
            <ul>
                <li>
                    <b>tonsky</b><br />
                    Links:
                    <External href="https://github.com/tonsky">GitHub</External> |
                    <External href="https://tonsky.me/">Website</External><br />
                </li>
            </ul>

            <p>
                License: <External href="https://github.com/tonsky/FiraCode/blob/master/LICENSE"
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

            <p>
                Links:
                <External href="https://fonts.google.com/noto/specimen/Noto+Sans"
                    >Google Fonts</External
                > |
                <External href="https://github.com/notofonts/latin-greek-cyrillic">GitHub</External>
                |
                <External href="https://notofonts.github.io/">Dashboard</External>
            </p>

            <p>Creator<span class="dim">(s)</span>:</p>
            <ul>
                <li>
                    <b>Noto Fonts Project</b><br />
                    Links:
                    <External href="https://github.com/notofonts">GitHub</External>
                </li>
            </ul>

            <p>
                License: <External
                    href="https://github.com/notofonts/latin-greek-cyrillic/blob/main/OFL.txt"
                    >SIL Open Font License 1.1</External
                >
            </p>

            <p>
                Identifier: <code>noto-sans</code>
            </p>

            <p>Usage: Used for general text and Unicode characters.</p>
        </div>

        <div class="font noto-sans-mono" id="noto-sans-mono">
            <h1>Noto Sans Mono</h1>

            <p>
                Links:
                <External href="https://fonts.google.com/noto/specimen/Noto+Sans+Mono"
                    >Google Fonts</External
                >
            </p>

            <p>Creator<span class="dim">(s)</span>:</p>
            <ul>
                <li>
                    <b>Noto Fonts Project</b><br />
                    Links:
                    <External href="https://github.com/notofonts">GitHub</External>
                </li>
            </ul>

            <p>
                License: <External
                    href="https://github.com/notofonts/latin-greek-cyrillic/blob/main/OFL.txt"
                    >SIL Open Font License 1.1</External
                >
            </p>

            <p>
                Identifier: <code>noto-sans-mono</code>
            </p>

            <p>Usage: Used for monospaced texts and headings.</p>
        </div>

        <div class="font geist" id="geist">
            <h1>Geist</h1>

            <p>
                Links:
                <External href="https://fonts.google.com/specimen/Geist">Google Fonts</External> |
                <External href="https://vercel.com/font">Website</External> |
                <External href="https://github.com/vercel/geist-font">GitHub</External>
            </p>

            <p>Creator<span class="dim">(s)</span>:</p>
            <ul>
                <li>
                    <b>Vercel</b><br />
                    Links:
                    <External href="https://vercel.com/home">Website</External>
                </li>
                <li>
                    Others: Andrés Briganti, Mateo Zaragoza, Guillermo Rauch, Evil Rabbit, José
                    Rago, Facundo Santana
                </li>
            </ul>

            <p>
                License: <External href="https://github.com/vercel/geist-font/blob/main/OFL.txt"
                    >SIL Open Font License 1.1</External
                >
            </p>

            <p>
                Identifier: <code>geist</code>
            </p>

            <p>Usage: Used for most text.</p>
        </div>
    </div>
</section>

<style lang="css">
    #showcase {
        overflow: visible;

        background: radial-gradient(circle at bottom center, rgba(100, 0, 255, 0.25), transparent),
            black;
        background-position: center center;
        background-attachment: fixed;
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

    .font {
        min-height: 100vh;
        width: 100%;

        display: flex;
        flex-direction: column;
        gap: 0.5em;
        justify-content: center;
    }
</style>
