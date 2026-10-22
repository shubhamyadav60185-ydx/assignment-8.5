## Aim
To build a complete responsive photo-gallery website using CSS Grid, including a header, navigation, multiple image cards, consistent gaps and a footer.

## Objectives
1. Create a website header and navigation bar.
2. Build a photo gallery using CSS Grid.
3. Display multiple image cards with titles and descriptions.
4. Use `repeat()`, `minmax()` and `fr` units.
5. Demonstrate named grid areas and explicit grid placement.
6. Prevent image and text overflow.
7. Test the website on different screen sizes.
8. Upload the completed project to GitHub.

## 1. Project Structure

Create a folder named `Assignment-8.5` and add these files:

```text
Assignment-8.5/
├── index.html
└── style.css
```

## 2. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta
        name="description"
        content="Explore beautiful travel, nature, architecture and lifestyle photography in our responsive photo gallery."
    >

    <title>FrameSpace | Photo Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Website Header -->
    <div class="page-layout">

        <header class="site-header">
            <a href="#home" class="logo">
                <span class="logo-icon">▧</span>
                FrameSpace
            </a>

            <nav class="navigation">
                <a href="#home">Home</a>
                <a href="#gallery">Gallery</a>
                <a href="#about">About</a>
            </nav>

            <a href="#gallery" class="header-button">Explore Photos</a>
        </header>

        <!-- Hero Section -->
        <section class="hero" id="home">
            <div class="hero-content">
                <p class="eyebrow">A COLLECTION OF MOMENTS</p>

                <h1>Discover the beauty of the world.</h1>

                <p class="hero-description">
                    Explore inspiring photographs of nature, travel,
                    architecture and everyday life.
                </p>

                <a href="#gallery" class="primary-button">
                    Explore Gallery &rarr;
                </a>
            </div>
        </section>

        <!-- Main Gallery Section -->
        <main class="gallery-section" id="gallery">

            <div class="section-heading">
                <div>
                    <p class="eyebrow">VISUAL STORIES</p>
                    <h2>Our Photo Gallery</h2>
                    <p class="section-description">
                        A little inspiration from every corner of the world.
                    </p>
                </div>

                <span class="photo-count">12 PHOTOS</span>
            </div>

            <div class="photo-grid">

                <!-- Featured Card -->
                <article class="photo-card featured-card">
                    <img
                        src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=1200&q=80"
                        alt="Mountain peaks surrounded by clouds"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">NATURE</span>
                        <h3>Mountains of Wonder</h3>
                        <p>Discover the quiet beauty of mountain landscapes.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=80"
                        alt="Scenic green landscape beneath a wide sky"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">TRAVEL</span>
                        <h3>Open Landscapes</h3>
                        <p>Beautiful views beyond the city.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1519501025264-65ba15a82390?auto=format&fit=crop&w=900&q=80"
                        alt="City skyline illuminated at night"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">CITY</span>
                        <h3>City Lights</h3>
                        <p>The energy of a city after dark.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=900&q=80"
                        alt="Peaceful lake surrounded by mountains"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">NATURE</span>
                        <h3>Peaceful Waters</h3>
                        <p>A calm escape beside the lake.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1511818966892-d7d671e672a2?auto=format&fit=crop&w=900&q=80"
                        alt="Modern architectural building"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">DESIGN</span>
                        <h3>Modern Architecture</h3>
                        <p>Creative forms and clean lines.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=900&q=80"
                        alt="Sunrise illuminating a natural landscape"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">SUNRISE</span>
                        <h3>Golden Morning</h3>
                        <p>A fresh beginning in warm light.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=900&q=80"
                        alt="Sunlight filtering through a green forest"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">FOREST</span>
                        <h3>Into the Forest</h3>
                        <p>Find inspiration among the trees.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=900&q=80"
                        alt="Blue ocean water meeting a sandy beach"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">OCEAN</span>
                        <h3>Ocean Escape</h3>
                        <p>Blue water and endless horizons.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?auto=format&fit=crop&w=900&q=80"
                        alt="Mountain valley with a beautiful lake"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">ADVENTURE</span>
                        <h3>Hidden Valleys</h3>
                        <p>Scenic destinations worth discovering.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1518837695005-2083093ee35b?auto=format&fit=crop&w=900&q=80"
                        alt="Ocean waves moving across the water"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">WATER</span>
                        <h3>Ocean Waves</h3>
                        <p>Nature's rhythm along the coast.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1493246507139-91e8fad9978e?auto=format&fit=crop&w=900&q=80"
                        alt="Green mountain scenery and a natural landscape"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">LANDSCAPE</span>
                        <h3>Green Horizons</h3>
                        <p>Fresh views across the countryside.</p>
                    </div>
                </article>

                <article class="photo-card">
                    <img
                        src="https://images.unsplash.com/photo-1472396961693-142e6e269027?auto=format&fit=crop&w=900&q=80"
                        alt="Wildlife in a natural outdoor environment"
                        loading="lazy"
                    >

                    <div class="photo-overlay">
                        <span class="photo-category">WILDLIFE</span>
                        <h3>Wild Encounters</h3>
                        <p>Appreciating wildlife in its natural home.</p>
                    </div>
                </article>

            </div>
        </main>

        <!-- About Section -->
        <section class="about-section" id="about">
            <div class="about-icon">✦</div>

            <div>
                <h2>Every picture tells a story.</h2>
                <p>
                    FrameSpace is a sample photography gallery created to
                    showcase beautiful images through a clean, responsive
                    and grid-based web design.
                </p>
            </div>
        </section>

        <!-- Footer -->
        <footer class="site-footer">
            <a href="#home" class="footer-logo">FrameSpace</a>

            <p>
                &copy; 2026 FrameSpace. Created with HTML and CSS Grid.
            </p>

            <a href="#home" class="back-to-top">Back to top ↑</a>
        </footer>

    </div>

</body>
</html>
```

## 3. CSS Code — `style.css`

```css
/* =========================
   1. GLOBAL STYLES
========================= */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary: #0f766e;
    --primary-dark: #115e59;
    --text-dark: #172b2a;
    --text-light: #647575;
    --background: #f5f8f7;
    --white: #ffffff;
    --border: #e1e9e6;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: var(--background);
    color: var(--text-dark);
    line-height: 1.6;
}

a {
    color: inherit;
}

img {
    display: block;
    max-width: 100%;
}

/* =========================
   2. OUTER GRID LAYOUT
========================= */

.page-layout {
    width: 100%;
    max-width: 1440px;
    min-height: 100vh;
    margin: 0 auto;

    display: grid;

    grid-template-columns: minmax(0, 1fr);

    grid-template-areas:
        "header"
        "hero"
        "gallery"
        "about"
        "footer";
}

/* =========================
   3. HEADER
========================= */

.site-header {
    grid-area: header;

    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;

    padding: 20px 5%;
    background-color: var(--white);
    border-bottom: 1px solid var(--border);
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;

    color: var(--text-dark);
    text-decoration: none;
    font-size: 1.5rem;
    font-weight: bold;
    white-space: nowrap;
}

.logo-icon {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 38px;
    height: 38px;
    border-radius: 10px;

    color: var(--white);
    background-color: var(--primary);
    font-size: 1.5rem;
}

.navigation {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 28px;
}

.navigation a {
    text-decoration: none;
    color: var(--text-light);
    font-weight: 600;
    font-size: 0.95rem;
}

.navigation a:hover {
    color: var(--primary);
}

.header-button {
    display: inline-block;
    padding: 10px 17px;

    background-color: var(--primary);
    color: var(--white);
    text-decoration: none;
    font-weight: bold;
    border-radius: 7px;

    transition: background-color 0.3s;
}

.header-button:hover,
.primary-button:hover {
    background-color: var(--primary-dark);
}

/* =========================
   4. HERO SECTION
========================= */

.hero {
    grid-area: hero;

    min-height: 340px;
    padding: 65px 7%;

    display: grid;
    grid-template-columns: minmax(0, 700px);
    align-content: center;

    background:
        linear-gradient(
            90deg,
            rgba(7, 35, 33, 0.88),
            rgba(7, 35, 33, 0.35)
        ),
        url("https://images.unsplash.com/photo-1470770841072-f978cf4d019e?auto=format&fit=crop&w=1800&q=85")
        center 45% / cover no-repeat;

    color: var(--white);
}

.hero-content {
    min-width: 0;
}

.eyebrow {
    color: #5eead4;
    font-size: 0.78rem;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 12px;
}

.hero h1 {
    max-width: 650px;
    font-size: clamp(2rem, 5vw, 3.8rem);
    line-height: 1.15;
    overflow-wrap: anywhere;
    margin-bottom: 18px;
}

.hero-description {
    max-width: 540px;
    color: #e2f2ef;
    font-size: 1.05rem;
    margin-bottom: 26px;
}

.primary-button {
    display: inline-block;
    padding: 12px 20px;

    background-color: var(--primary);
    color: var(--white);
    text-decoration: none;
    font-weight: bold;
    border-radius: 7px;

    transition: background-color 0.3s;
}

/* =========================
   5. GALLERY SECTION
========================= */

.gallery-section {
    grid-area: gallery;
    padding: 60px 5%;
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    flex-wrap: wrap;
    gap: 18px;

    margin-bottom: 28px;
}

.section-heading .eyebrow {
    color: var(--primary);
}

.section-heading h2 {
    color: var(--text-dark);
    font-size: clamp(1.7rem, 3vw, 2.3rem);
    line-height: 1.25;
    margin-bottom: 8px;
}

.section-description {
    color: var(--text-light);
}

.photo-count {
    display: inline-block;
    color: var(--primary-dark);
    background-color: #d9f4ee;
    padding: 7px 12px;
    border-radius: 6px;

    font-size: 0.8rem;
    font-weight: bold;
    white-space: nowrap;
}

/* PRIMARY PHOTO GRID */

.photo-grid {
    display: grid;

    /* repeat(), minmax() and fr units */
    grid-template-columns: repeat(4, minmax(0, 1fr));

    gap: 22px;
    grid-auto-flow: dense;
}

/* PHOTO CARDS */

.photo-card {
    position: relative;
    isolation: isolate;
    min-width: 0;
    min-height: 260px;

    overflow: hidden;
    border-radius: 12px;
    background-color: #dce8e5;
    box-shadow: 0 5px 18px rgba(15, 50, 45, 0.08);
}

/* Explicit grid placement for featured card */
.featured-card {
    grid-column: span 2;
    grid-row: span 2;
    min-height: 542px;
}

.photo-card img {
    width: 100%;
    height: 100%;
    min-height: inherit;

    object-fit: cover;
    object-position: center;

    transition: transform 0.5s ease;
}

.photo-card:hover img {
    transform: scale(1.06);
}

/* Gradient keeps text readable over images */
.photo-card::after {
    content: "";
    position: absolute;
    inset: 0;
    z-index: 0;

    background: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.82) 0%,
        rgba(0, 0, 0, 0.25) 45%,
        transparent 75%
    );
}

.photo-overlay {
    position: absolute;
    z-index: 1;
    left: 0;
    right: 0;
    bottom: 0;

    padding: 20px;
    color: var(--white);
    overflow-wrap: anywhere;
}

.photo-category {
    display: inline-block;
    color: #ffffff;
    background-color: rgba(15, 118, 110, 0.9);

    padding: 4px 8px;
    margin-bottom: 9px;
    border-radius: 4px;

    font-size: 0.68rem;
    font-weight: bold;
    letter-spacing: 1px;
}

.photo-overlay h3 {
    font-size: 1.15rem;
    line-height: 1.3;
    margin-bottom: 6px;
}

.photo-overlay p {
    color: #e2e8e7;
    font-size: 0.85rem;
    line-height: 1.5;
}

.featured-card .photo-overlay {
    padding: 28px;
}

.featured-card .photo-overlay h3 {
    font-size: clamp(1.5rem, 3vw, 2.2rem);
}

/* =========================
   6. ABOUT SECTION
========================= */

.about-section {
    grid-area: about;

    display: flex;
    align-items: center;
    gap: 22px;

    margin: 0 5% 55px;
    padding: 30px;

    background-color: #e5f4ef;
    border: 1px solid #cce9df;
    border-radius: 12px;
}

.about-icon {
    display: flex;
    align-items: center;
    justify-content: center;

    flex-shrink: 0;
    width: 55px;
    height: 55px;

    color: var(--white);
    background-color: var(--primary);
    border-radius: 12px;
    font-size: 1.8rem;
}

.about-section h2 {
    margin-bottom: 7px;
    font-size: 1.4rem;
}

.about-section p {
    color: var(--text-light);
    max-width: 760px;
    overflow-wrap: anywhere;
}

/* =========================
   7. FOOTER
========================= */

.site-footer {
    grid-area: footer;

    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;

    padding: 25px 5%;
    background-color: #102d2a;
    color: #d1e5e0;
}

.footer-logo {
    color: var(--white);
    font-size: 1.15rem;
    font-weight: bold;
    text-decoration: none;
}

.site-footer p {
    font-size: 0.85rem;
}

.back-to-top {
    color: #5eead4;
    font-size: 0.9rem;
    text-decoration: none;
}

.back-to-top:hover {
    text-decoration: underline;
}

/* =========================
   8. TABLET RESPONSIVENESS
========================= */

@media (max-width: 1000px) {
    .site-header {
        padding: 18px 4%;
    }

    .navigation {
        gap: 16px;
    }

    .gallery-section {
        padding: 45px 4%;
    }

    .photo-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 18px;
    }

    .featured-card {
        grid-column: span 2;
        grid-row: span 2;
        min-height: 500px;
    }

    .photo-card {
        min-height: 240px;
    }

    .about-section {
        margin-left: 4%;
        margin-right: 4%;
    }
}

/* =========================
   9. MOBILE RESPONSIVENESS
========================= */

@media (max-width: 650px) {
    .site-header {
        justify-content: center;
        text-align: center;
        padding: 18px 5%;
    }

    .logo {
        width: 100%;
        justify-content: center;
    }

    .navigation {
        width: 100%;
        gap: 20px;
    }

    .header-button {
        display: none;
    }

    .hero {
        min-height: 310px;
        padding: 45px 6%;
    }

    .hero-description {
        font-size: 0.95rem;
    }

    .gallery-section {
        padding: 38px 5%;
    }

    .photo-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
        gap: 14px;
    }

    .featured-card {
        grid-column: span 2;
        grid-row: span 1;
        min-height: 340px;
    }

    .photo-card {
        min-height: 230px;
    }

    .photo-overlay {
        padding: 13px;
    }

    .photo-overlay h3 {
        font-size: 1rem;
    }

    .photo-overlay p {
        font-size: 0.78rem;
    }

    .featured-card .photo-overlay {
        padding: 20px;
    }

    .about-section {
        align-items: flex-start;
        margin: 0 5% 35px;
        padding: 20px;
        gap: 15px;
    }

    .about-icon {
        width: 42px;
        height: 42px;
        font-size: 1.3rem;
    }

    .about-section h2 {
        font-size: 1.15rem;
    }

    .site-footer {
        justify-content: center;
        flex-direction: column;
        text-align: center;
        padding: 25px 5%;
    }
}

/* =========================
   10. SMALL MOBILE SCREENS
========================= */

@media (max-width: 380px) {
    .photo-grid {
        grid-template-columns: minmax(0, 1fr);
    }

    .featured-card {
        grid-column: span 1;
        grid-row: span 1;
        min-height: 300px;
    }

    .photo-card {
        min-height: 280px;
    }

    .section-heading {
        align-items: flex-start;
        flex-direction: column;
    }

    .navigation {
        gap: 14px;
    }

    .navigation a {
        font-size: 0.85rem;
    }
}
```

## 4. Explanation of CSS Grid Properties

### A. `display: grid`

It converts an element into a grid container, allowing its child elements to be arranged in rows and columns.

```css
.photo-grid {
    display: grid;
}
```

### B. `repeat()`, `minmax()` and `fr`

```css
.photo-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 22px;
}
```

- `repeat(4, ...)` creates four columns.
- `minmax(0, 1fr)` allows each column to shrink when needed while sharing the available space equally.
- `fr` represents a fraction of the available space.
- `gap: 22px` maintains consistent spacing between cards.

### C. Named Grid Areas

The outer page uses named grid areas:

```css
.page-layout {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    grid-template-areas:
        "header"
        "hero"
        "gallery"
        "about"
        "footer";
}
```

Each section is assigned its own area:

```css
.site-header {
    grid-area: header;
}

.hero {
    grid-area: hero;
}

.gallery-section {
    grid-area: gallery;
}

.about-section {
    grid-area: about;
}

.site-footer {
    grid-area: footer;
}
```

### D. Explicit Grid Placement

The featured photo occupies two columns and two rows on larger screens:

```css
.featured-card {
    grid-column: span 2;
    grid-row: span 2;
}
```

This gives the featured image greater visual importance than the other cards.

### E. Preventing Overflow

```css
.photo-card {
    min-width: 0;
    overflow: hidden;
}

.photo-card img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.photo-overlay {
    overflow-wrap: anywhere;
}
```

These rules keep images inside their cards and allow long text to wrap instead of overflowing.

## 5. How to Run the Project

1. Open Visual Studio Code.
2. Open the `Assignment-8.5` folder.
3. Create `index.html` and `style.css`.
4. Paste the complete HTML and CSS code into their respective files.
5. Save both files.
6. Open `index.html` in a browser or use the Live Server extension.
7. Keep an internet connection available for the externally hosted images.

## 6. Responsive Testing

Test the website at the following approximate viewport widths:

| Device | Width | Expected layout |
|---|---:|---|
| Desktop | 1200px | Four gallery columns |
| Tablet | 800px | Three gallery columns |
| Mobile | 500px | Two gallery columns |
| Small mobile | 360px | One gallery column |

Use Chrome DevTools to resize the viewport and check that images remain within cards, text wraps properly, and no horizontal page overflow occurs.

## 7. Expected Output

The completed website contains:

- A header with a logo and navigation.
- A hero section with a title and call-to-action link.
- A photo gallery with 12 image cards.
- A featured image spanning multiple grid cells on larger screens.
- Consistent spacing between cards.
- An About section and footer.
- Responsive layouts for desktop, tablet and mobile devices.

## 8. GitHub Submission

### Step 1: Create a GitHub Repository

1. Visit https://github.com/
2. Sign in to your account.
3. Click **New repository**.
4. Enter the repository name `Assignment-8.5`.
5. Select **Public** if your assignment requires a public repository.
6. Create the repository.

### Step 2: Upload the Project Using Git

Open the VS Code terminal inside your project folder and run:

```bash
git init
git add index.html style.css
git commit -m "Complete CSS Grid photo gallery project"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/Assignment-8.5.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

If Git says that a remote named `origin` already exists, check it with:

```bash
git remote -v
```

Use the correct repository URL before pushing. GitHub may ask you to authenticate before the upload completes.

### Step 3: Submit the GitHub Link

After successfully pushing the project, open your repository on GitHub and copy its URL.

Your submission should include:

- `index.html`
- `style.css`
- A screenshot of the completed website, if required
- Your actual GitHub repository URL

**GitHub repository link:** `https://github.com/YOUR-USERNAME/Assignment-8.5`

Replace the placeholder with your real username and confirm that the repository is accessible before submitting.

## 9. Result

A complete responsive photo-gallery website was created using HTML5 and CSS Grid. The project demonstrates `repeat()`, `minmax()`, `fr` units, named grid areas, explicit grid placement, consistent gaps, overflow prevention and responsive columns. The project can be tested locally and uploaded to GitHub for submission.
