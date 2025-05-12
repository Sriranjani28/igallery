# Ex.05 Design of Interactive Image Gallery
## Date:12.05.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Image Gallery</title>
  <style>
    body {
      margin: 0;
      padding: 20px;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #FFDEE9, #B5FFFC); /* Softer gradient */
      text-align: center;
    }

    h1 {
      color: #2C3E50;
      margin-bottom: 25px;
      font-size: 3rem;
      letter-spacing: 1px;
    }

    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;
        max-width: 1000px;
        margin: auto;
        padding: 10px;
    }


    .gallery img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 12px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: pointer;
    }

    .gallery img:hover {
      transform: scale(1.07);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.25);
    }

    .lightbox {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .lightbox img {
      max-width: 85%;
      max-height: 85%;
      border-radius: 12px;
      box-shadow: 0 0 40px rgba(255, 255, 255, 0.3);
      animation: fadeIn 0.4s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .footer {
      margin-top: 60px;
      color: #34495E;
      font-weight: bold;
      font-size: 1.2rem;
    }
  </style>
</head>
<body>

  <h1>Interactive Image Gallery</h1>

  <div class="gallery">
    <img src="image 1.jpg" alt="Image 1">
    <img src="image 2.jpg" alt="Image 2">
    <img src="image 3.jpg" alt="Image 3">
    <img src="image 4.jpg" alt="Image 4">
    <img src="image 5.jpg" alt="Image 5">
    <img src="image 6.jpg" alt="Image 6">
  </div>

  <div class="lightbox" id="lightbox">
    <img id="lightbox-img" src="" alt="Full View">
  </div>

  <hr style="margin-top: 80px; border: none; height: 2px; background: #aaa;">

  <div class="footer">
    Name: Sriranjani M<br><br>
    Register No: 212224040327
  </div>

  <script>
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const galleryImgs = document.querySelectorAll('.gallery img');

    galleryImgs.forEach(img => {
      img.addEventListener('click', () => {
        lightboxImg.src = img.src;
        lightbox.style.display = 'flex';
      });
    });

    lightbox.addEventListener('click', () => {
      lightbox.style.display = 'none';
    });
  </script>

</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot (6).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
