- 👋 Hi, I’m @Marm-m
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Marm-m/Marm-m is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple Photo Gallery</title>
<style>
  .gallery-container {
    width: 80%;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
  .photo {
    margin: 5px;
    border: 1px solid #ccc;
    float: left;
    width: 300px;
    height: 200px;
    background-position: center;
    background-size: cover;
    transition: transform 0.2s;
  }
  .photo:hover {
    transform: scale(1.1);
  }
</style>
</head>
<body>

<div id="gallery" class="gallery-container">
  <!-- Photos will be inserted here -->
</div>

<button onclick="prevPhoto()">Previous</button>
<button onclick="nextPhoto()">Next</button>

<script>
// Array of image URLs
const photos = [
  'photo1.jpg',
  'photo2.jpg',
  'photo3.jpg',
  // Add more photo URLs
];

let currentPhotoIndex = 0;

function displayPhoto(index) {
  const gallery = document.getElementById('gallery');
  gallery.innerHTML = '<div class="photo" style="background-image: url(' + photos[index] + ');"></div>';
}

function prevPhoto() {
  if (currentPhotoIndex > 0) {
    currentPhotoIndex--;
    displayPhoto(currentPhotoIndex);
  }
}

function nextPhoto() {
  if (currentPhotoIndex < photos.length - 1) {
    currentPhotoIndex++;
    displayPhoto(currentPhotoIndex);
  }
}

// Initial display
displayPhoto(currentPhotoIndex);
</script>

</body>
</html>
