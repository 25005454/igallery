# Ex.07 Design of Interactive Image Gallery
## Date:27/12/2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```
gallery.html

<html>
<head>
    
    <title>Interactive Image Gallery</title> 
    <link rel="stylesheet" href="gallery.css">
</head>  
<body> 
<div class="gallery-container"> 
<img id="galleryImage" class="gallery-image" src="2 ph.png" height="10%" width="10%"> 
<div id="caption" class="caption">Caption for Image 1</div> 
<div class="gallery-buttons"> 
<button onclick="prevImage()">Previous</button> 
<button onclick="nextImage()">Next</button> 
</div> 
</div> 
<script> 
const images = [ 
{ src: "2 ph.png", caption: "Caption for Image 1" }, 
{ src: "3 ph.png", caption: "Caption for Image 2" }, 
{ src: "Screenshot 2025-12-27 085333.png", caption: "Caption for Image 3" }, 
{ src: "Screenshot 2025-12-27 084903.png", caption: "Caption for Image 4" } 
]; 
let currentIndex = 0; 
function updateGallery( )  
{ 
document.getElementById("galleryImage").src = images[currentIndex].src; 
document.getElementById("caption").textContent = images[currentIndex].caption; 
} 
function nextImage( )  
{ 
currentIndex = (currentIndex + 1) % images.length; 
updateGallery( ); 
} 
function prevImage( )  
{ 
currentIndex = (currentIndex - 1 + images.length) % images.length; 
updateGallery( ); 
} 
</script> 

<footer>
     E.vamsi krishna (25005454)
</footer>
</body>
</html>

gallery.css


         .gallery-container  
{ 
            position: relative; 
            max-width: 600px; 
            margin: auto; 
            background: rgb(255, 255, 255); 
            padding: 10px; 
            border-radius: 10px; 
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); 
         } 
         .gallery-image  
{ 
            width: 100%; 
            height: 400px; 
            object-fit: cover; 
            border-radius: 10px; 
         } 
         .caption  
{ 
            margin-top: 30px; 
            font-size: 18px; 
         } 
         .gallery-buttons  
{ 
            display: flex; 
            justify-content: space-between; 
            margin-top: 20px; 
         } 
         button  
{ 
            padding: 10px 20px; 
            cursor: pointer; 
            border: none; 
            border-radius: 5px; 
            background-color: rgb(59, 59, 241); 
            color: rgb(255, 255, 255); 
            transition: 0.3s; 
         } 
     

         footer {
         text-align: center;
         padding: 10px;
         background: rgb(156, 156, 156);
         font-size: 14px;

}

```
## OUTPUT:
![alt text](<src 1.png>)
![alt text](<src 2.png>)
![alt text](<src 3.png>)
![alt text](<src 4.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
