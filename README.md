<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flower Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #fefefe;
      margin: 0;
      padding: 20px;
    }
    h1 {
      color: #ff69b4;
    }
    #flower-img {
      width: 300px;
      height: auto;
      border-radius: 12px;
      margin: 20px 0;
    }
    button {
      background: #ff69b4;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.2s;
    }
    button:hover {
      transform: scale(1.1);
    }
    #qr-container {
      margin-top: 30px;
    }
    canvas {
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>Welcome to My Flower Page 🌸</h1>
  <img id="flower-img" src="cat.jpg" alt="Flower Image">

  <div>
    <button id="open-letter">Open Special Letter</button>
  </div>

  <div id="qr-container">
    <h3>Scan QR to visit this page</h3>
    <canvas id="qr-code"></canvas>
  </div>

  <!-- QR code library -->
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>

  <script>
    // Open letter button action
    document.getElementById("open-letter").addEventListener("click", () => {
      alert("This is your special letter! 🌸💌");
    });

    // Generate QR code pointing to this GitHub Pages URL
    const qrCanvas = document.getElementById("qr-code");
    const pageUrl = "https://YOUR_USERNAME.github.io/YOUR_REPO/"; // <-- CHANGE THIS
    QRCode.toCanvas(qrCanvas, pageUrl, { width: 150 }, function (error) {
      if (error) console.error(error);
    });
  </script>
</body>
</html>
