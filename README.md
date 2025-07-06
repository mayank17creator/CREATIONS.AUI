# CREATIONS.AUI
I will write blogs
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MAYANK CREATIONS</title>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      height: 100vh;
      background: radial-gradient(circle at bottom, #0f2027, #203a43, #2c5364);
      font-family: 'Outfit', sans-serif;
      overflow: hidden;
      color: white;
    }

    .container {
      position: relative;
      width: 100%;
      height: 100%;
      overflow: hidden;
    }

    .title-box {
      text-align: center;
      margin-top: 80px;
      z-index: 100;
      position: relative;
    }

    h1 {
      font-size: 3rem;
      letter-spacing: 2px;
      margin-bottom: 10px;
      background: linear-gradient(90deg, #00f2ff, #ffffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    p {
      font-size: 1.2rem;
      color: #ccc;
    }

    .cylinder {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 100px;
      height: 120px;
      background: linear-gradient(to top, rgba(0,242,255,0.4), rgba(255,255,255,0.1));
      backdrop-filter: blur(5px);
      border-radius: 50px 50px 0 0;
      border: 2px solid rgba(255,255,255,0.3);
      box-shadow: 0 0 30px rgba(0,242,255,0.4);
      z-index: 10;
    }

    .bubbles {
      position: absolute;
      bottom: 100px;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }

    .bubble {
      position: absolute;
      bottom: 0;
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(4px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 0 10px rgba(255,255,255,0.15);
      color: white;
      font-weight: bold;
      text-align: center;
      line-height: 90px;
      animation: rise 4.5s ease-in infinite;
      font-size: 0.9rem;
    }

    .bubble:nth-child(1) { left: 10%; animation-delay: 0s; }
    .bubble:nth-child(2) { left: 25%; animation-delay: 1s; }
    .bubble:nth-child(3) { left: 40%; animation-delay: 2s; }
    .bubble:nth-child(4) { left: 55%; animation-delay: 3s; }
    .bubble:nth-child(5) { left: 70%; animation-delay: 0.5s; }
    .bubble:nth-child(6) { left: 85%; animation-delay: 1.5s; }

    @keyframes rise {
      0% { transform: translateY(0) scale(1); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translateY(-110vh) scale(1.3); opacity: 0; }
    }

    /* === LOGIN FORM === */
    .login-box {
      position: absolute;
      top: 55%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 320px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 30px;
      box-shadow: 0 0 20px rgba(0,255,255,0.15);
      z-index: 99;
    }

    .login-box h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #00f2ff;
    }

    .login-box input {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: none;
      border-radius: 10px;
      outline: none;
      background: rgba(255,255,255,0.1);
      color: white;
      font-size: 0.95rem;
    }

    .login-box button {
      width: 100%;
      padding: 10px;
      background: #00f2ff;
      border: none;
      border-radius: 10px;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }

    .login-box button:hover {
      background: #00d4e0;
    }

    .login-box .switch {
      text-align: center;
      margin-top: 10px;
      font-size: 0.9rem;
      color: #ccc;
      cursor: pointer;
    }

    .hidden { display: none; }

    @media (max-width: 600px) {
      h1 { font-size: 2rem; }

      .bubble {
        width: 60px;
        height: 60px;
        line-height: 60px;
        font-size: 0.7rem;
      }

      .cylinder {
        width: 70px;
        height: 90px;
      }

      .login-box {
        width: 90%;
        padding: 20px;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="title-box">
      <h1>Welcome to MAYANK CREATIONS</h1>
      <p>Your AI that’s fast, smart, and creative.</p>
    </div>

    <div class="bubbles">
      <div class="bubble">Smart</div>
      <div class="bubble">Creative</div>
      <div class="bubble">Reliable</div>
      <div class="bubble">Fast</div>
      <div class="bubble">24/7</div>
      <div class="bubble">Human-like</div>
    </div>

    <div class="cylinder"></div>

    <!-- Login Box -->
    <div class="login-box" id="loginForm">
      <h2>Login</h2>
      <input type="text" placeholder="Email">
      <input type="password" placeholder="Password">
      <button>Login</button>
      <div class="switch" onclick="switchForm()">Create an Account</div>
    </div>

    <!-- Signup Box -->
    <div class="login-box hidden" id="signupForm">
      <h2>Create Account</h2>
      <input type="text" placeholder="Full Name">
      <input type="email" placeholder="Email">
      <input type="password" placeholder="Password">
      <button>Create</button>
      <div class="switch" onclick="switchForm()">Already have an account?</div>
    </div>
  </div>

  <script>
    function switchForm() {
      const login = document.getElementById("loginForm");
      const signup = document.getElementById("signupForm");
      login.classList.toggle("hidden");
      signup.classList.toggle("hidden");
    }
  </script>

</body>
</html>
