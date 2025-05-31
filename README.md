<html lang="lt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mano internetinis viešas turinys</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    /* Base styles for the body */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Inter', sans-serif; /* Using Inter font */
      color: #f0f0f0; /* Light text color */
      min-height: 100vh; /* Ensures background covers full height */
      display: flex;
      flex-direction: column;
      justify-content: flex-start; /* Align content to the top */
      align-items: center;
      /* Background image settings */
      /* Change 'path/to/your/background_image.jpg' to your background image path */
      background-image: url('https://placehold.co/1920x1080/000000/FFFFFF?text=Jūsų+fono+paveikslėlis+čia'); /* Change this URL to your background image path */
      background-size: cover; /* Cover the entire background */
      background-position: center; /* Center the image */
      background-repeat: no-repeat; /* Do not repeat the image */
      background-attachment: fixed; /* Image fixed when scrolling the page */
      background-color: #222; /* Fallback background color if image fails to load */
    }

    /* Container styles */
    .container {
      background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent black background */
      padding: 40px 60px; /* Inner spacing */
      max-width: 960px; /* Maximum width */
      width: 90%; /* Adapts to screen width */
      border-radius: 15px; /* Rounded corners */
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5); /* Shadow */
      text-align: center;
      box-sizing: border-box; /* Includes padding and border in element's width/height */
      margin-top: 50px; /* Add margin to the top to push content down */
      margin-bottom: 50px; /* Add margin to the bottom */
    }

    /* Heading styles */
    h1 {
      text-align: center; /* Center text */
      margin-bottom: 40px; /* Bottom margin */
      font-size: 2.5em; /* Larger font size */
      color: #00ccff; /* Brighter heading color */
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* Text shadow */
    }

    /* Links container, arranged as a vertical list of cards */
    .links-list {
      display: flex;
      flex-direction: column; /* Stack cards vertically */
      gap: 25px; /* Space between cards */
      margin-top: 30px;
    }

    /* Styles for each map card */
    .map-card {
      background-color: rgba(50, 50, 50, 0.9); /* Slightly more opaque background for cards */
      border-radius: 12px; /* Rounded corners */
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.4); /* Shadow */
      overflow: hidden; /* Hides overflowing content, e.g., rounded corners for image */
      transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transitions */
      display: flex; /* Use flexbox for internal layout (image and content side-by-side) */
      flex-direction: row; /* Image and content side-by-side */
      align-items: center; /* Vertically align items in the card */
      text-decoration: none; /* Remove underline from the card if it's a link */
      color: #f0f0f0; /* Text color inside the card */
    }

    .map-card:hover {
      transform: translateY(-5px); /* Slightly lift the card on hover */
      box-shadow: 0 12px 25px rgba(0, 204, 255, 0.4); /* Brighter shadow */
    }

    /* Thumbnail image style */
    .map-thumbnail {
      width: 250px; /* Fixed width for the thumbnail */
      height: 150px; /* Fixed height for the thumbnail */
      object-fit: cover; /* Ensures image fills the space */
      flex-shrink: 0; /* Prevents thumbnail from shrinking */
      border-right: 2px solid #00ccff; /* Separator line */
    }

    /* Content area within the card */
    .map-card-content {
      padding: 20px;
      text-align: left; /* Align text to the left */
      flex-grow: 1; /* Allows content to take remaining space */
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    /* Link text inside the card */
    .map-card-content a {
      color: #fff; /* White text color */
      text-decoration: none; /* Remove underline */
      font-size: 1.3em; /* Larger font size for the link */
      transition: color 0.3s ease;
      display: flex; /* Allows icon and text to be on one line */
      align-items: center; /* Vertically center icon and text */
      justify-content: flex-start; /* Align content to the left */
    }

    .map-card-content a:hover {
      color: #00ccff; /* Blue color on hover */
    }

    /* Font Awesome icon styles inside the card */
    .map-card-content .fas {
      margin-right: 12px; /* Space between icon and text */
      font-size: 1.2em; /* Icon size */
      color: #00ccff; /* Icon color */
    }

    /* Responsive adjustments */
    @media (max-width: 768px) {
      .container {
        padding: 30px;
        margin: 30px auto;
      }

      h1 {
        font-size: 2em;
      }

      .map-card {
        flex-direction: column; /* Stack image and content vertically on small screens */
        align-items: center;
      }

      .map-thumbnail {
        width: 100%; /* Thumbnail takes full width */
        height: 180px; /* Adjust height for better display */
        border-right: none; /* Remove right border */
        border-bottom: 2px solid #00ccff; /* Add bottom border */
      }

      .map-card-content {
        padding: 15px;
        text-align: center; /* Center text on small screens */
      }

      .map-card-content a {
        font-size: 1.1em;
        justify-content: center; /* Center content on small screens */
      }
    }

    @media (max-width: 480px) {
      .container {
        padding: 20px;
        margin: 20px auto;
      }

      h1 {
        font-size: 1.8em;
        margin-bottom: 20px;
      }

      .map-thumbnail {
        height: 150px;
      }

      .map-card-content a {
        font-size: 1em;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Mano internetinis viešas turinys</h1>
    <div class="links-list">
      <div class="map-card">
        <img src="https://placehold.co/250x150/4A90E2/FFFFFF?text=1+Žemėlapis" alt="1 Žemėlapis" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_1.html" target="_blank"><i class="fas fa-map"></i> 1 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://placehold.co/250x150/50E3C2/FFFFFF?text=2+Žemėlapis" alt="2 Žemėlapis" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_2.html" target="_blank"><i class="fas fa-map"></i> 2 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://placehold.co/250x150/F5A623/FFFFFF?text=3+Žemėlapis" alt="3 Žemėlapis" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_3.html" target="_blank"><i class="fas fa-map"></i> 3 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://placehold.co/250x150/BD10E0/FFFFFF?text=Geoportal" alt="Geoportal žemėlapis" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/2_praktinis/zhemelapyzas.html" target="_blank"><i class="fas fa-map"></i> Geoportal žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://placehold.co/250x150/7ED321/FFFFFF?text=ArcGIS" alt="ArcGIS aplikacija" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/3_praktinis/appsas.html" target="_blank"><i class="fas fa-map"></i> ArcGIS aplikacija</a>
        </div>
      </div>
    </div>
  </div>
</body>
</html>