# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```

<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: #f4f4f4;
        }
        h1 {
            margin: 20px 0;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            padding: 20px;
            width: 100%;
            max-width: 1200px;
        }
        .gallery img {
            width: 100%;
            height: auto;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.2s ease-in-out;
        }
        .gallery img:hover {
            transform: scale(1.05);
        }
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }
        .lightbox.active {
            display: flex;
        }
        .close {
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 30px;
            color: white;
            background: transparent;
            border: none;
            cursor: pointer;
        }
        .close:hover {
            color: #f00;
        }
    </style>
</head>
<body>
    <h1>Interactive Image Gallery</h1>
    <div class="gallery">
        <img src="i1.jpg" data-full="i1.jpg" alt="Image 1">
        <img src="i2.jpg" data-full="i2.jpg" alt="Image 2">
        <img src="i3.jpg" data-full="i3.jpg" alt="Image 3">
        <img src="i4.jpg" data-full="i4.jpg" alt="Image 4">
        <img src="i5.jpg" data-full="i5.jpg" alt="Image 5">
        <img src="i6.jpg" data-full="i6.jpg" alt="Image 6">
        <img src="i7.jpg" data-full="i7.jpg" alt="Image 7">
        <img src="i8.jpg" data-full="i7.jpg" alt="Image 8">
        <img src="i9.jpg" data-full="i7.jpg" alt="Image 9">
    </div>
    <div id="lightbox" class="lightbox">
        <img id="lightbox-img" src="" alt="Expanded Image">
        <button class="close" id="lightbox-close">&times;</button>
    </div>
    <script>
        const galleryImages = document.querySelectorAll('.gallery img');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = document.getElementById('lightbox-img');
        const lightboxClose = document.getElementById('lightbox-close');

        galleryImages.forEach(image => {
            image.addEventListener('click', () => {
                lightboxImg.src = image.getAttribute('data-full');
                lightbox.classList.add('active');
            });
        });

        lightboxClose.addEventListener('click', () => {
            lightbox.classList.remove('active');
        });

        lightbox.addEventListener('click', (e) => {
            if (e.target === lightbox) {
                lightbox.classList.remove('active');
            }
        });
    </script>
</body>
</html>
```


## OUTPUT
<img width="1920" height="1080" alt="Screenshot 2025-11-17 213944" src="https://github.com/user-attachments/assets/60968aef-3bd2-498f-bf7d-04a74c3b08bb" />


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
