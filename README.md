<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Birthday Celebration Page</title>
  <style>
    body {
      margin: 0;
      background-color: #ffcce0; /* Pink background */
      font-family: Arial, sans-serif;
    }
    .container {
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    #image {
      width: 400px;
      height: 400px;
      opacity: 0;
      transition: opacity 2s ease-in;
      cursor: grab;
      position: absolute;
    }
    #image:hover {
      transform: scale(1.05);
      transition: transform 0.3s ease-in-out;
    }
    .sides {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
    .balloon, .confetti, .star, .cupcake, .ribbon {
      position: absolute;
      animation: float 5s infinite ease-in-out;
    }
    /* Balloons */
    .balloon {
      width: 60px;
      height: 100px;
      background: radial-gradient(circle, #ff99cc, #ff6699);
      border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      box-shadow: 2px 4px 8px rgba(0, 0, 0, 0.2);
    }
    .balloon:nth-child(1) { left: 10%; top: 20%; animation-delay: 0s; }
    .balloon:nth-child(2) { left: 80%; top: 30%; animation-delay: 1s; }
    .balloon:nth-child(3) { left: 15%; top: 70%; animation-delay: 2s; }
    .balloon:nth-child(4) { left: 85%; top: 60%; animation-delay: 3s; }
    /* Confetti */
    .confetti {
      width: 5px;
      height: 15px;
      background-color: #ffcc00;
      border-radius: 2px;
      animation: fall 3s infinite linear;
    }
    .confetti:nth-child(5) { left: 40%; top: 10%; animation-delay: 0.5s; }
    .confetti:nth-child(6) { left: 50%; top: 15%; animation-delay: 1s; }
    .confetti:nth-child(7) { left: 60%; top: 20%; animation-delay: 1.5s; }
    .confetti:nth-child(8) { left: 30%; top: 25%; animation-delay: 2s; }
    /* Stars */
    .star {
      width: 20px;
      height: 20px;
      background-color: #ffffff;
      clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
      box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.2);
      animation: twinkle 2s infinite;
    }
    .star:nth-child(9) { left: 25%; top: 15%; animation-delay: 0.3s; }
    .star:nth-child(10) { left: 70%; top: 25%; animation-delay: 1s; }
    .star:nth-child(11) { left: 45%; top: 65%; animation-delay: 0.8s; }
    /* Cupcake */
    .cupcake {
      width: 80px;
      height: 100px;
      background: linear-gradient(to bottom, #fff2cc, #ffcc99);
      border-radius: 0 0 20px 20px;
      position: absolute;
      bottom: 10px;
    }
    .cupcake:before {
      content: '';
      position: absolute;
      top: -30px;
      left: 10px;
      width: 60px;
      height: 40px;
      background: radial-gradient(circle, #ff99cc, #ff6699);
      border-radius: 50%;
    }
    .cupcake:nth-child(12) { left: 5%; animation: none; }
    .cupcake:nth-child(13) { right: 5%; animation: none; }
    /* Ribbon */
    .ribbon {
      width: 100px;
      height: 20px;
      background: linear-gradient(to bottom, #ff6699, #ff3366);
      position: absolute;
    }
    .ribbon:nth-child(14) { top: 5%; left: 50%; transform: rotate(-45deg); }
    .ribbon:nth-child(15) { top: 5%; right: 50%; transform: rotate(45deg); }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-30px); }
    }
    @keyframes fall {
      0% { transform: translateY(0) rotate(0); }
      100% { transform: translateY(300px) rotate(360deg); }
    }
    @keyframes twinkle {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.5; }
    }
    .text-container {
      position: absolute;
      bottom: 20px;
      width: 100%;
      text-align: center;
      font-size: 24px;
      color: #ff6699;
      font-weight: bold;
    }
  </style>
</head>
<body>

<div class="container">
  <img id="image" src="https://scontent.fmnl4-8.fna.fbcdn.net/v/t1.15752-9/467474413_1668196007062105_6079642840431097976_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=9f807c&_nc_eui2=AeGZcys9SOGjmPFjwlJQYGdwr4nr-badmqeviev5tp2ap5hIEv66e1N_3SHjuIHOuVSUUvi4uruzloS_y1ZK8BMi&_nc_ohc=FudBYJfwci8Q7kNvgFHBFVP&_nc_zt=23&_nc_ht=scontent.fmnl4-8.fna&oh=03_Q7cD1QEGiCMKniuvf0jWe9Kt_YmbHLYRIvx0Kaz_0BUHqiSemA&oe=676D5A30" alt="Birthday Image">
  <div class="sides">
    <!-- Balloons -->
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <!-- Confetti -->
    <div class="confetti"></div>
    <div class="confetti"></div>
    <div class="confetti"></div>
    <div class="confetti"></div>
    <!-- Stars -->
    <div class="star"></div>
    <div class="star"></div>
    <div class="star"></div>
    <!-- Cupcakes -->
    <div class="cupcake"></div>
    <div class="cupcake"></div>
    <!-- Ribbons -->
    <div class="ribbon"></div>
    <div class="ribbon"></div>
  </div>
</div>

<div class="text-container">
  Happy Birthday! 🎉 Have an amazing year ahead! 🌟
</div>

<audio id="music" src="https://www.youtube.com/watch?v=O2aQhWwxuyY" autoplay loop></audio>

<script>
  // Slowly display the image
  const image = document.getElementById("image");
  setTimeout(() => {
    image.style.opacity = 1;
  }, 1000);

  // Enable dragging of the image
  let isDragging = false;
  let offset = { x: 0, y: 0 };

  image.addEventListener("mousedown", (e) => {
    isDragging = true;
    offset.x = e.clientX - image.offsetLeft;
    offset.y = e.clientY - image.offsetTop;
    image.style.cursor = "grabbing";
  });

  document.addEventListener("mouseup", () => {
    isDragging = false;
    image.style.cursor = "grab";
  });

  document.addEventListener("mousemove", (e) => {
    if (isDragging) {
      image.style.left = `${e.clientX - offset.x}px`;
      image.style.top = `${e.clientY - offset.y}px`;
    }
  });

  // Automatically play music
  const music = document.getElementById("music");
  music.play();
</script>

</body>
</html>
