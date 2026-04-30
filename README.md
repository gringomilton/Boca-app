# Boca-app
Boca app
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Boca App</title>
  <style>
    body {
      margin: 0;
      font-family: Arial;
      background: #0a1f44;
      color: white;
      text-align: center;
    }

    .container {
      padding: 20px;
    }

    input {
      padding: 10px;
      margin: 10px;
      width: 80%;
      border-radius: 5px;
      border: none;
    }

    button {
      padding: 10px 20px;
      background: #fdd835;
      border: none;
      border-radius: 5px;
      font-weight: bold;
    }

    .hidden {
      display: none;
    }

    h1 {
      color: #fdd835;
    }
  </style>
</head>
<body>

<div class="container" id="login">
  <h1>Boca App 💙💛</h1>
  <input type="text" id="user" placeholder="Usuario"><br>
  <input type="password" id="pass" placeholder="Contraseña"><br>
  <button onclick="login()">Entrar</button>
</div>

<div class="container hidden" id="home">
  <h1>Bienvenido Hincha 🔥</h1>
  <p>¡Aguante Boca!</p>
  <button onclick="logout()">Salir</button>
</div>

<script>
function login() {
  const user = document.getElementById("user").value;
  const pass = document.getElementById("pass").value;

  if(user === "boca" && pass === "1234") {
    document.getElementById("login").classList.add("hidden");
    document.getElementById("home").classList.remove("hidden");
  } else {
    alert("Datos incorrectos");
  }
}

function logout() {
  document.getElementById("home").classList.add("hidden");
  document.getElementById("login").classList.remove("hidden");
}
</script>

</body>
</html>