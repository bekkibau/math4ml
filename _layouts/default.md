<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ page.title }}</title>

    <!-- Load KaTeX -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.css">
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/katex.min.js"></script>
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.0/dist/contrib/auto-render.min.js"
            onload="renderMathInElement(document.body);"></script>

    <!-- Optional: Slightly Adjust KaTeX Font Size -->
    <style>
        .katex { font-size: 1.1em; } /* Adjust as needed */
    </style>
</head>
<body>

    <header>
        <h1>{{ page.title }}</h1>
        <nav>
            <a href="/">Home</a> | 
            <a href="/katex-workarounds.md">KaTeX Workarounds</a>
        </nav>
        <hr>
    </header>

    <main>
        {{ content }}
    </main>

</body>
</html>