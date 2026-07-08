ALLIES, LLC — WEBSITE FILES
============================

WHAT'S IN HERE
- index.html         → Home page
- about.html          → About page
- get-started.html    → Get Started page
- contact.html        → Contact page
- styles.css          → All colors, fonts, and layout — shared by every page
- script.js           → Mobile menu + footer year — shared by every page
- images/             → Put your real photos in here
- files/              → Put your referral-form.pdf in here once you have one

HOW TO PREVIEW
Double-click any .html file to open it in your browser. Click around —
the nav links between all 4 pages work locally too.

HOW TO EDIT
Open any file in a text editor (VS Code is a free, beginner-friendly option:
code.visualstudio.com). Search for "EDIT ME" comments — those mark every
spot with placeholder text, links, or images you should replace with your
real content.

IMPORTANT: the header (top nav) and footer (bottom bar) are repeated in
all 4 HTML files. If you want to change your phone number, address, or
nav links, you'll need to update it in each of the 4 files.

ADDING YOUR OWN PHOTOS
1. Convert any iPhone photos from HEIC to JPEG first (ask Claude if needed).
2. Drop the .jpg files into the images/ folder.
3. In the HTML, find the matching placeholder, e.g.:
     <img src="images/placeholder.svg" alt="...">
   and change just the src to your filename:
     <img src="images/my-photo.jpg" alt="...">

HOW TO PUBLISH FOR FREE
Go to app.netlify.com/drop and drag this ENTIRE FOLDER (or a zip of it)
into the browser window. You'll get a free live URL in seconds.

CONTROLLING IMAGE OPACITY & DARKNESS
Every <img> on the site can be faded or darkened individually, right from
the HTML — no separate CSS rule needed per image. Add a style attribute
like this to any image tag:

    <img src="images/my-photo.jpg" alt="..." style="--img-opacity: 0.85; --img-brightness: 0.6;">

  --img-opacity:    1   = fully visible (default).  0.5 = half-faded.  0 = invisible.
  --img-brightness: 1   = normal (default).  Below 1 = darker (0.6 is noticeably dim).
                     Above 1 = lighter/washed out (1.3 = brighter than normal).

You can set just one of the two if you only want to change darkness OR
opacity, not both.

HERO PHOTO DARKNESS (home page background image)
The dark tint over the hero photo (so the white text stays readable) is
controlled in styles.css near the top, in the :root section:

    --hero-overlay-top: rgba(28,43,58,0.55);
    --hero-overlay-bottom: rgba(28,43,58,0.8);

The last number in each (0.55 and 0.8) is the darkness — 0 is no tint at
all (photo fully visible), 1 is solid navy (photo invisible). Raise both
numbers for a darker, moodier hero; lower them if your photo is getting
too obscured.

CONTROLLING PHOTO SIZE (About page "Why Choose Us" photos)
Each of the 4 photos next to your reasons can be resized individually.
Add a style attribute to that specific <img> tag:

    <img src="images/my-photo.jpg" alt="..." style="--img-w: 80%; --img-ratio: 1 / 1;">

  --img-w:      how wide the photo is within its column. 100% = fills
                the column (default). 60% = noticeably smaller.
  --img-ratio:  the width-to-height shape. 4 / 3 = standard photo shape
                (default). 1 / 1 = perfect square. 16 / 9 = wide/short.

You only need to set the ones you want to change — leave the other out
to keep its default.

