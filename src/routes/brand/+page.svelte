<section>
    <h1>Lanzaforge Branding Guidelines</h1>

    <h2 id="writing-lanzaforge">Writing "Lanzaforge"</h2>

    <p>
        <b>Lanzaforge</b> is always written as a single word with a capital L. No spaces or alternative
        capitalization should be used.
    </p>

    <p>Examples of unacceptable use include:</p>

    <ul>
        <li>LanzaForge.</li>
        <li>Lanza forge.</li>
        <li>Lanza Forge.</li>
        <li>lanzaforge. <b>This is only accepted in URL names and handles.</b></li>
        <li>LANZAFORGE.</li>
    </ul>

    <h2 id="logos">Lanzaforge Logos</h2>

    <p>The only official Lanzaforge logo currently available is the text logo.</p>

    <p>
        An image-based logo may be added in the future. This section will be updated accordingly if
        one is introduced.
    </p>

    <h3 id="normal-logo">Normal Logo</h3>

    <p>Please use this version of the logo whenever possible.</p>

    <ul>
        <li>
            <b>Typeface:</b> Geist
        </li>
        <li>
            <b>Font weight:</b> 400 (Regular)
        </li>
        <li>
            <b>"Lanza" color:</b> <a href="#primary-purple">Primary Purple</a>
        </li>
        <li>
            <b>"forge" color:</b> <a href="#secondary-silver">Secondary Silver</a>
        </li>
    </ul>

    <div class="text-logo">
        <div class="logo">
            <span class="head">Lanza</span><span class="tail">forge</span>
        </div>
    </div>

    <h3 id="modified-logos">Modified Logos</h3>

    <p>
        On busy backgrounds, you may color the logo to be either white (<code>#ffffff</code>) or
        black (<code>#000000</code>).
    </p>

    <h3 id="logo-guidelines">Logo Guidelines</h3>

    <p>
        The Lanzaforge logo should always remain recognizable and consistent with the official
        design. When reproducing the logo, follow these guidelines:
    </p>

    <ul>
        <li>
            <b>Do not change the typeface.</b><br />
            The logo must use Geist.
        </li>

        <li>
            <b>Do not change the font weight.</b><br />
            The logo must use the Regular (400) weight.
        </li>

        <li>
            <b>Do not alter the capitalization.</b><br />
            The logo must always be written as <b>Lanzaforge</b>.
        </li>

        <li>
            <b>Do not distort the logo.</b><br />
            Do not stretch, compress, rotate, skew, or otherwise alter its proportions.
        </li>

        <li>
            <b>Do not apply visual effects.</b><br />
            Do not add shadows, outlines, gradients, glows, or other effects to the logo.<br />
            Opacity may be applied to certain interactive elements when appropriate.
        </li>

        <li>
            <b>Do not substitute brand colors.</b><br />
            The normal logo should use the official
            <a href="#primary-purple">Primary Purple</a> and
            <a href="#secondary-silver">Secondary Silver</a> colors.
        </li>

        <li>
            <b>Keep the logo legible.</b><br />
            Avoid placing the logo on backgrounds where it is difficult to read. Use the
            <a href="#modified-logos">modified logos</a> when necessary.
        </li>

        <li>
            <b>Maintain sufficient space around the logo.</b><br />
            Do not place text, images, or other visual elements too close to the logo.
        </li>
    </ul>

    <h2 id="brand-colors">Lanzaforge Brand Colors</h2>

    <div class="colors">
        <div class="color" id="primary-purple">
            <h3>
                <div class="color-block logo-primary"></div>
                <p>
                    <code>#6400ff</code> - <b>Primary Purple</b>
                </p>
            </h3>

            <p>Usage: primary brand color, emphasized text</p>
        </div>

        <div class="color" id="secondary-silver">
            <h3>
                <div class="color-block logo-secondary"></div>
                <p>
                    <code>#777777</code> - <b>Secondary Silver</b>
                </p>
            </h3>

            <p>Usage: secondary brand color</p>
        </div>
    </div>

    <p>
        When reproducing the Lanzaforge text logo in color, use only the official color values
        above. Do not approximate, substitute, modify, tint, or apply effects to the logo.
    </p>
</section>

<style>
    .colors {
        display: flex;
        flex-direction: column;
        gap: 2em;
    }

    .colors .color {
        display: flex;
        flex-direction: column;
        align-items: flex-start;

        gap: 0.5em;
    }

    .colors .color h3 {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 0.5em;
    }

    .color-block {
        display: inline-block;
        background: #111;
        width: 1.5em;
        height: 1.5em;
        border: 1px solid rgba(255, 255, 255, 0.5);
        border-radius: 2147483647px;
    }

    .color-block.logo-primary {
        background: #6400ff;
    }

    .color-block.logo-secondary {
        background: #777;
    }

    .text-logo {
        text-align: center;
        font-size: 5em;
        font-weight: 400;
    }
</style>
