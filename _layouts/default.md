<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>

    <!-- Load KaTeX Styles -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.css">
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.js"></script>
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/contrib/auto-render.min.js"
            onload="renderMathInElement(document.body, {delimiters: [
                {left: '$$', right: '$$', display: true},  // Block equations
                {left: '$', right: '$', display: false}    // Inline equations
            ]});">
    </script>
    <!-- Apply KaTeX Font Globally -->

    <style>
        /* Use KaTeX's default font for everything */
        body {
            font-family: KaTeX_Main, serif;
            font-size: 1.05rem;
            padding: 20px;
            line-height: 1.6;
        }

        /* Ensure headers also use KaTeX font */
        h1, h2, h3, h4, h5, h6 {
            font-family: KaTeX_Main, serif;
            font-weight: normal;
        }

        /* Improve inline math spacing */
        .katex {
            font-size: 1.1em;
        }

        /* Ensure block math is well-spaced */
        .katex-display {
            margin: 1rem 0;
        }
    </style>

</head>
<body>

<header>
    <h1>{{ page.title }}</h1>
    <nav>
        <a href="/">Home</a> |
        <a href="/tags.md/">Tags</a>
    </nav>
    <hr>
</header>

    <main>
        {{ content }}
    </main>

</body>
</html>
