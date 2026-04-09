MONSE'S TASTE OF EL SALVADOR — Images Folder
=============================================

Place your image files in this folder. The filenames below match
the references used in the HTML and CSS files.

REQUIRED IMAGES
---------------
hero-bg.jpg
  Used as: Full-screen hero background on the Home page
  Recommended: Restaurant exterior, building mural, or your best food photo
  Size: At least 1600×900px, landscape orientation
  Referenced in: css/styles.css (.hero-bg background-image)

favicon.png
  Used as: Browser tab icon
  Recommended: Monse's logo or a simple 'M' icon
  Size: 32×32px or 64×64px PNG with transparent background
  Uncomment the <link rel="icon"> tag in each HTML file's <head>

OPTIONAL / ADDITIONAL PHOTOS
-----------------------------
Add any additional photos here using descriptive filenames, then
reference them in gallery.html to replace the placeholder boxes.

Suggested photos to add:
  exterior-front.jpg         — Restaurant front entrance / street view
  exterior-mural.jpg         — The colorful Monse's building mural
  dining-room.jpg            — Interior dining room wide shot
  patio-seating.jpg          — Outdoor dog-friendly patio
  kitchen-prep.jpg           — Kitchen or food preparation
  pupusa-plate.jpg           — Plated pupusas with curtido
  team-photo.jpg             — Owner / team photo
  ambiance-detail.jpg        — Interior decor or cultural details
  brunch-spread.jpg          — Weekend brunch dishes

HOW TO SWAP IN YOUR IMAGES
---------------------------
In gallery.html, look for comments like:
  <!-- REPLACE: restaurant exterior photo -->
Replace the <div class="gallery-placeholder"> block with:
  <img src="images/your-photo-name.jpg" alt="Description of photo" />

In about.html, events.html, look for:
  <div class="img-placeholder story-img-placeholder" ...>
Replace the entire div with:
  <img src="images/your-photo.jpg" alt="Description" class="about-img-main" />

IMAGE OPTIMIZATION TIPS
------------------------
- Use JPG for photos, PNG for logos/icons with transparency
- Compress images before uploading (recommended: TinyJPG.com or Squoosh.app)
- Target file sizes: hero < 400KB, gallery images < 200KB each
- Always include descriptive alt text for accessibility

CURRENT PHOTOS (already in use via external URLs)
--------------------------------------------------
These photos are currently loaded from TripAdvisor and Squarespace CDN.
If those URLs ever break, download the photos and host them locally here.

  Building mural:     images.squarespace-cdn.com/...building+mural+logo.jpg
  Dining interior:    media-cdn.tripadvisor.com/...23/3f/2e/8e/caption.jpg
  Pupusas on plate:   media-cdn.tripadvisor.com/...28/f3/82/e2/caption.jpg
  Single pupusa:      media-cdn.tripadvisor.com/...25/24/88/bb/caption.jpg
  Curtido:            media-cdn.tripadvisor.com/...25/24/88/bc/caption.jpg
  Tostada:            media-cdn.tripadvisor.com/...23/3f/2e/8d/caption.jpg
  Table view:         media-cdn.tripadvisor.com/...1d/03/a4/26/photo0jpg.jpg
  Strawberry Mojito:  images.squarespace-cdn.com/...Strawberry+Mojito+2.jpg
  Traditional Plate:  images.squarespace-cdn.com/...Traditional%2C+Skillet...jpg
