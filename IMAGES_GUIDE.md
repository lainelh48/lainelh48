# How to Add Photos to Your Portfolio

## Step 1: Create an Images Directory
1. In GitHub, create a new folder in your repository called `images` or `assets`
2. This is where you'll store all your project photos and diagrams

## Step 2: Upload Your Images
1. Go to your repository on GitHub
2. Navigate to the `images` folder
3. Click "Add file" → "Upload files"
4. Select your image files (JPG, PNG, GIF, SVG, etc.)
5. Commit the changes

## Step 3: Add Images to Project Pages

### For a Single Image:
```html
<div class="project-image">
    <img src="../images/project-name.jpg" alt="Description of the image">
</div>
```

### For Multiple Images (Gallery):
```html
<div class="project-gallery">
    <img src="../images/image1.jpg" alt="First image description">
    <img src="../images/image2.jpg" alt="Second image description">
    <img src="../images/image3.jpg" alt="Third image description">
</div>
```

### For Hero/Header Image:
```html
<div class="project-hero">
    <img src="../images/satellite-hero.jpg" alt="CANX-2 Satellite illustration">
</div>
```

## Step 4: Update the Project Pages
Each project page has comments showing where to add images. Look for:
```html
<!-- HOW TO ADD PHOTOS:
     1. Create an 'images' folder in your repo
     2. Upload your photo file
     3. Use the img tag with the correct path
-->
```

Uncomment the image block and update the path and alt text.

## Example: Adding to CANX-2 Satellite Project

**File:** `projects/canx2-satellite.html`

Find this section:
```html
<!-- <div class="project-image">
    <img src="../images/satellite-diagram.jpg" alt="CANX-2 Satellite Link Simulator diagram">
</div> -->
```

Uncomment it and make sure you have `images/satellite-diagram.jpg` in your repo.

## Image Path Guide

- **From root-level pages** (index.html, projects.html): `images/filename.jpg`
- **From project pages** (projects/canx2-satellite.html): `../images/filename.jpg` (go up one folder)

## File Size Tips
- Keep images under 2MB for faster loading
- Recommended dimensions:
  - Hero images: 1200px wide
  - Project images: 800px wide
  - Thumbnails: 300px wide

## Supported Image Formats
- **JPG/JPEG** - Best for photos
- **PNG** - Best for diagrams, transparent backgrounds
- **GIF** - For animations
- **SVG** - For vectors/diagrams
- **WebP** - Modern format, smaller file size

## CSS Styling Available

Your project pages have built-in classes for image styling:
- `.project-image` - Single image container
- `.project-gallery` - Multiple image gallery
- `.project-hero` - Large header image

You can add custom CSS to `styles/styles.css` if needed:
```css
.project-image img,
.project-gallery img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    margin: 20px 0;
}
```

## Example Repository Structure
```
lainelh48/
├── index.html
├── about.html
├── projects.html
├── experience.html
├── contact.html
├── styles/
│   └── styles.css
├── projects/
│   ├── canx2-satellite.html
│   ├── ultrasound-motor.html
│   ├── octe.html
│   ├── pulse-oximeter.html
│   ├── ecg-monitor.html
│   └── mechatronics-robot.html
└── images/          ← Create this folder
    ├── satellite-diagram.jpg
    ├── ultrasound-ui.jpg
    ├── motor-control.jpg
    ├── pulse-ox-device.jpg
    ├── ecg-monitor.jpg
    └── robot-photo.jpg
```

## Next Steps
1. Create the `images` folder
2. Upload your project photos
3. Uncomment the image blocks in each project page
4. Update the file paths to match your image names
5. Update the alt text for accessibility
