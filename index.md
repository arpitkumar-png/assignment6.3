File 1: overflow-practice.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 6.3 — Overflow & Layout Fixing</title>
    <!-- Link to External Stylesheet -->
    <link rel="stylesheet" href="overflow-style.css">
</head>
<body>

    <!-- Header -->
    <header class="page-header">
        <h1>CSS Overflow & Layout Fixing</h1>
        <p>Demonstrating visible, hidden, auto, and scroll behaviors on fixed-height containers.</p>
    </header>

    <main class="container">
        
        <!-- 1, 2, 3. Overflow Visible -->
        <section class="overflow-card">
            <h2>1. overflow: visible (Default)</h2>
            <p class="description">Content overflows out of the box boundaries without being clipped.</p>
            <div class="box overflow-visible">
                <p>This is a fixed-height container with a lot of text inside it. Because the overflow property is set to visible, the excess text spills completely out of the box container and overlaps whatever is underneath it on the webpage.</p>
            </div>
        </section>

        <!-- 1, 2, 3. Overflow Hidden -->
        <section class="overflow-card">
            <h2>2. overflow: hidden</h2>
            <p class="description">Excess content is clipped and hidden from view entirely.</p>
            <div class="box overflow-hidden">
                <p>This is a fixed-height container with a lot of text inside it. Because the overflow property is set to hidden, any text that exceeds the box height is abruptly clipped and invisible to the user, preventing layout breakage.</p>
            </div>
        </section>

        <!-- 1, 2, 3, 4. Overflow Auto -->
        <section class="overflow-card">
            <h2>3. overflow: auto</h2>
            <p class="description">Scrollbars appear automatically only when content overflows.</p>
            <div class="box overflow-auto">
                <p>This is a fixed-height container with plenty of text inside it. Because overflow is set to auto, the browser automatically provides a clean vertical scrollbar so users can read the rest of the text without breaking the page layout.</p>
                <p>Additional paragraph text to ensure scrolling is triggered smoothly inside this container box.</p>
            </div>
        </section>

        <!-- 1, 2, 3. Overflow Scroll -->
        <section class="overflow-card">
            <h2>4. overflow: scroll</h2>
            <p class="description">Scrollbars are permanently rendered on the box whether needed or not.</p>
            <div class="box overflow-scroll">
                <p>This is a fixed-height container with text. The overflow property is set to scroll, which forces scrollbars to appear on the box container at all times.</p>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Student Overflow & Layout Lab. All rights reserved.</p>
    </footer>

</body>
</html>
File 2: overflow-style.css
CSS
/* --- Global Reset & Typography --- */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
    padding: 2rem;
}

/* --- Header Styling --- */
.page-header {
    text-align: center;
    margin-bottom: 2.5rem;
}

.page-header h1 {
    color: #1e293b;
    font-size: 2rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    color: #64748b;
}

/* --- Main Container --- */
.container {
    max-width: 700px;
    margin: 0 auto;
}

/* --- Card Wrapper --- */
.overflow-card {
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 1.5rem;
    margin-bottom: 1.5rem;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.02);
}

.overflow-card h2 {
    font-size: 1.2rem;
    color: #1e3a8a;
    margin-bottom: 0.25rem;
}

.description {
    font-size: 0.9rem;
    color: #64748b;
    margin-bottom: 1rem;
}

/* --- Base Box Style (Fixed Height Container) --- */
.box {
    width: 100%;
    height: 90px;                  /* 1. Fixed height container */
    background-color: #f1f5f9;
    border: 2px solid #cbd5e1;
    border-radius: 6px;
    padding: 0.75rem;
    font-size: 0.9rem;
    color: #334155;
}

/* --- 3. Overflow Property Values --- */

/* Visible (Default behavior) */
.overflow-visible {
    overflow: visible;
}

/* Hidden (Crops overflow) */
.overflow-hidden {
    overflow: hidden;
}

/* Auto (Scrollbars appear only when content overflows) */
.overflow-auto {
    overflow: auto;
}

/* Scroll (Scrollbars always present) */
.overflow-scroll {
    overflow: scroll;
}