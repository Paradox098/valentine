<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      text-align: center;
      background-color: #ffd5e5; /* Light pink background */
      margin: 0;
    }

    #container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    h1 {
      color: #ff66a3; /* Pink text */
      margin-bottom: 10px;
    }

    #yesButton {
      font-size: 24px;
      padding: 20px 40px;
      margin: 10px;
      cursor: pointer;
      transition: font-size 0.5s, padding 0.5s;
      background-color: #ff66a3; /* Pink button */
      color: white;
      border: none;
      border-radius: 15px;
    }

    #noButton {
      font-size: 16px;
      padding: 10px 20px;
      margin: 10px;
      cursor: pointer;
      background-color: #ff66a3; /* Pink button */
      color: white;
      border: none;
      border-radius: 15px;
    }

    #message {
      display: none;
      margin-top: 20px;
    }

    #valentineImage, #homepageImage {
      max-width: 100%;
      height: auto;
      border-radius: 15px;
      margin-top: 20px;
      border: 5px solid #ff66a3; /* Pink border */
    }
  </style>
</head>
<body>

<div id="container">
  <img id="homepageImage" src="https://4kwallpapers.com/images/wallpapers/kawaii-couple-cute-2048x2048-10100.png" alt="Attractive Image" width="350px">
  <h1>Will you be my Valentine, Akshata? 💖</h1>
  <button id="yesButton" onclick="showMessage()">Yes</button>
  <button id="noButton" onclick="increaseNoButton()">No</button>
  <div id="message">
    <p>Yay! You said yes! 😍</p>
    <img id="valentineImage" src="https://media1.tenor.com/m/jjM8wEXXNqwAAAAd/kiss.gif" alt="Cute bear kissing">
    <p>Wait, Akshata, I'm coming! 😍</p>
  </div>
</div>

<script>
   let yesButtonSize = 24; // Initial size of the "Yes" button

  function increaseYesButton() {
    yesButtonSize += 5; // Increase the size by 5 pixels
    document.getElementById('yesButton').style.fontSize = yesButtonSize + 'px';
  }

  let noButtonClicks = 0;

  function increaseNoButton() {
    noButtonClicks++;
    document.getElementById('noButton').innerHTML = getNoButtonText();
    increaseYesButton(); // Increase the size of "Yes" button each time "No" is clicked
  }

  function getNoButtonText() {
    const options = [
      "Are you sure, cutu? 🙄",
      "Please budu, don't do that to me!",
      "Maybe reconsider, cutu?",
      "Think about it!",
      "Manoj will cry! 😭😭",
      "Don't break my heart! 😔😔"
    ];

    return options[noButtonClicks % options.length];
  }

  function showMessage() {
    document.getElementById('yesButton').style.display = 'none';
    document.getElementById('noButton').style.display = 'none';
    document.getElementById('message').style.display = 'block';
  }
</script>

</body>
</html>
