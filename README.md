<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday My Love ❤️</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, sans-serif;
    }

    body{
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      background:linear-gradient(135deg,#ff758c,#ff7eb3);
      overflow:hidden;
      position:relative;
    }

    /* Floating Hearts */
    .heart{
      position:absolute;
      color:rgba(255,255,255,0.7);
      font-size:20px;
      animation:float 6s linear infinite;
    }

    @keyframes float{
      0%{
        transform:translateY(100vh) scale(0);
        opacity:0;
      }
      50%{
        opacity:1;
      }
      100%{
        transform:translateY(-10vh) scale(1.5);
        opacity:0;
      }
    }

    /* Main Card */
    .card{
      background:white;
      width:360px;
      padding:40px 30px;
      border-radius:25px;
      text-align:center;
      box-shadow:0 10px 40px rgba(0,0,0,0.25);
      animation:fadeIn 1.5s ease;
      z-index:2;
    }

    .card h1{
      color:#ff4d6d;
      font-size:36px;
      margin-bottom:15px;
    }

    .card p{
      color:#555;
      font-size:18px;
      line-height:1.7;
      margin-bottom:25px;
    }

    .love{
      font-size:60px;
      animation:beat 1s infinite;
      margin-bottom:15px;
    }

    @keyframes beat{
      0%,100%{
        transform:scale(1);
      }
      50%{
        transform:scale(1.2);
      }
    }

    button{
      padding:14px 28px;
      border:none;
      border-radius:50px;
      background:#ff4d6d;
      color:white;
      font-size:17px;
      cursor:pointer;
      transition:0.3s;
      box-shadow:0 5px 15px rgba(255,77,109,0.4);
    }

    button:hover{
      background:#e63956;
      transform:scale(1.08);
    }

    @keyframes fadeIn{
      from{
        opacity:0;
        transform:translateY(30px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    /* Popup */
    .popup{
      position:fixed;
      top:0;
      left:0;
      width:100%;
      height:100%;
      background:rgba(0,0,0,0.65);
      display:flex;
      justify-content:center;
      align-items:center;
      animation:fadePopup 0.5s ease;
      z-index:1000;
    }

    .popup-box{
      background:white;
      width:340px;
      padding:35px 25px;
      border-radius:25px;
      text-align:center;
      animation:popupAnim 0.5s ease;
      box-shadow:0 10px 35px rgba(0,0,0,0.3);
    }

    .popup-box h2{
      color:#ff4d6d;
      margin-bottom:15px;
      font-size:30px;
    }

    .popup-box p{
      color:#555;
      line-height:1.8;
      font-size:18px;
    }

    .popup-box button{
      margin-top:20px;
    }

    @keyframes popupAnim{
      from{
        transform:scale(0.5);
        opacity:0;
      }
      to{
        transform:scale(1);
        opacity:1;
      }
    }

    @keyframes fadePopup{
      from{
        opacity:0;
      }
      to{
        opacity:1;
      }
    }
  </style>
</head>
<body>

  <!-- Floating Hearts -->
  <div class="heart" style="left:10%; animation-duration:5s;">❤️</div>
  <div class="heart" style="left:30%; animation-duration:7s;">💖</div>
  <div class="heart" style="left:50%; animation-duration:6s;">💕</div>
  <div class="heart" style="left:70%; animation-duration:8s;">❤️</div>
  <div class="heart" style="left:90%; animation-duration:5s;">💖</div>

  <!-- Main Card -->
  <div class="card">
    <div class="love">❤️</div>

    <h1>Happy Birthday Jaan 🎂</h1>

    <p>
      Tum meri zindagi ki sabse khoobsurat wajah ho 💖<br><br>
      Allah tumhe hamesha khush rakhe ✨<br>
      I Love You Forever ❤️
    </p>

    <button onclick="showMessage()">
      Open Surprise 🎁
    </button>
  </div>

  <!-- JavaScript -->
  <script>
    function showMessage(){

      const popup = document.createElement("div");
      popup.classList.add("popup");

      popup.innerHTML = `
        <div class="popup-box">
          <h2>💌 For My Love</h2>

          <p>
            Happy Birthday Meri Jaan ❤️<br><br>
            Tumhari smile meri duniya hai ✨<br>
            Main hamesha tumhare saath rahunga 💖<br><br>
            Love You So Much ❤️
          </p>

          <button onclick="closePopup()">
            Close 💕
          </button>
        </div>
      `;

      document.body.appendChild(popup);
    }

    function closePopup(){
      document.querySelector(".popup").remove();
    }
  </script>

</body>
</html>
