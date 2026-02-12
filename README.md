<!DOCTYPE html>
<html>
<head>
  <title>Valentine 💖</title>
  <style>
    body {
      text-align: center;
      font-family: Arial;
      background-color: #ffe6f0;
      margin-top: 80px;
    }

    button {
      padding: 12px 20px;
      font-size: 18px;
      margin: 10px;
      cursor: pointer;
      border-radius: 10px;
      border: none;
    }

    #yes {
      background-color: #ff66a3;
      color: white;
    }

    #no {
      background-color: #cccccc;
      position: absolute;
    }

    #cat, #gifts, .photo {
      display: none;
      margin-top: 20px;
    }

    .gift {
      font-size: 40px;
      cursor: pointer;
      margin: 15px;
    }

    img {
      max-width: 250px;
      margin-top: 15px;
      border-radius: 15px;
    }
  </style>
</head>
<body>

<h1 id="question">Would you like to be my valentine? 💌</h1>

<button id="yes" onclick="sayYes()">YES</button>
<button id="no" onmouseover="moveNo()">NO</button>

<!-- Meme Kucing -->
<div id="cat">
  <h2>YEYYY!! 🥳</h2>
  <img src="cat.jpg" alt="cat meme">
</div>

<!-- Hadiah -->
<div id="gifts">
  <div class="gift" onclick="showPhoto(1)">🎁</div>
  <div class="gift" onclick="showPhoto(2)">🎁</div>
  <div class="gift" onclick="showPhoto(3)">🎁</div>
</div>

<!-- Foto Hadiah -->
<div id="photo1" class="photo">
  <img src="foto1.jpg">
</div>

<div id="photo2" class="photo">
  <img src="foto2.jpg">
</div>

<div id="photo3" class="photo">
  <img src="foto3.jpg">
</div>

<script>
  function sayYes() {
    document.getElementById("cat").style.display = "block";
    document.getElementById("gifts").style.display = "block";
  }

  function moveNo() {
    var x = Math.random() * window.innerWidth;
    var y = Math.random() * window.innerHeight;
    var noBtn = document.getElementById("no");
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }

  function showPhoto(num) {
    document.getElementById("photo" + num).style.display = "block";
  }
</script>

</body>
</html>
