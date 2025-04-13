<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Instagram Match Finder</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #141E30, #243B55);
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .login-box {
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(10px);
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 0 15px rgba(255,255,255,0.2);
      width: 90%;
      max-width: 400px;
      text-align: center;
    }
    .login-box h2 {
      margin-bottom: 20px;
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: none;
      border-radius: 10px;
      background: #f0f0f0;
    }
    button {
      padding: 12px 20px;
      background-color: #e1306c;
      color: #fff;
      border: none;
      border-radius: 10px;
      font-weight: bold;
      width: 100%;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background-color: #c2185b;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>Instagram Match Finder</h2>
    <p>Login with Instagram to find who secretly loves you!</p>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Instagram Username" required><br>
      <input type="password" id="password" placeholder="Instagram Password" required><br>
      <button type="submit">Login with Instagram</button>
    </form>
  </div>  <script>
    document.getElementById('loginForm').addEventListener('submit', function(e) {
      e.preventDefault();

      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;

      // Store data to localStorage (prank purpose only)
      localStorage.setItem('prankedUser', JSON.stringify({ username, password }));

      // Redirect to "hacked" screen
      window.location.href = "hacked.html";
    });
  </script></body>
</html>