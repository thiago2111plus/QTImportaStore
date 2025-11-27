<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>QTImportaStore</title>
  <meta name="description" content="QTImportaStore.com - La página más decorativa y divertida de internet.">
  <style>
    body{
      margin:0;
      font-family:Inter, sans-serif;
      background:linear-gradient(135deg,#ffd6e8,#d6e8ff,#fff3c4);
      min-height:100vh;
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:flex-start;
      text-align:center;
      padding:40px 20px;
    }
    h1{
      font-size:48px;
      margin-bottom:10px;
      font-weight:800;
      color:#333;
    }
    p{
      max-width:540px;
      font-size:18px;
      color:#444;
      margin-bottom:28px;
    }
    .btn{
      background:#111;
      color:white;
      padding:18px 36px;
      border-radius:16px;
      font-size:20px;
      font-weight:700;
      border:0;
      cursor:pointer;
      transition:0.15s;
      margin-bottom:28px;
    }
    .btn:hover{
      transform:scale(1.05);
      background:#000;
    }
    .section{
      width:100%;
      max-width:1000px;
      margin-bottom:40px;
      text-align:left;
    }
    .product{
      display:flex;
      flex-direction:column;
      align-items:center;
      margin-bottom:20px;
    }
    .product img{
      width:180px;
      height:180px;
      object-fit:cover;
      border-radius:12px;
      margin-bottom:8px;
      transition:0.3s;
    }
    .product img:hover{
      transform:scale(1.1);
    }
    .images{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
      gap:20px;
      width:100%;
      max-width:1000px;
    }
    .popup{
      position:fixed;
      top:0; left:0;
      width:100%; height:100%;
      background:rgba(0,0,0,0.65);
      display:flex;
      align-items:center;
      justify-content:center;
      opacity:0;
      pointer-events:none;
      transition:0.3s;
    }
    .popup.active{
      opacity:1;
      pointer-events:auto;
    }
    .popup-box{
      background:white;
      padding:40px;
      border-radius:20px;
      font-size:28px;
      font-weight:800;
      max-width:480px;
      color:#000;
      box-shadow:0 12px 40px rgba(0,0,0,0.25);
      text-align:center;
    }
  </style>
</head>
<body>
  <h1>QTImportaStore</h1>
  <p>Bienvenido a <strong>QTImportaStore.com</strong>, la página menos útil y más decorativa de internet. Nada de lo que ves aquí sirve, pero se ve bonito.</p>

  <button class="btn" onclick="showMsg()">Ver mercancía</button>

  <div class="section">
    <h2>Productos Destacados</h2>
    <div class="images">
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,shirt" alt="Camiseta aesthetic">
        <p>Camiseta Aesthetic</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,jacket" alt="Chaqueta aesthetic">
        <p>Chaqueta Aesthetic</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,bag" alt="Bolso aesthetic">
        <p>Bolso Aesthetic</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,shoes" alt="Zapatos aesthetic">
        <p>Zapatos Aesthetic</p>
      </div>
    </div>
  </div>

  <div class="section">
    <h2>Decoración y Objetos</h2>
    <div class="images">
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,decor" alt="Decoración">
        <p>Decoración Aesthetic</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,accessory" alt="Accesorio">
        <p>Accesorio Aesthetic</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,plant" alt="Planta decorativa">
        <p>Planta Decorativa</p>
      </div>
      <div class="product">
        <img src="https://source.unsplash.com/200x200/?aesthetic,lights" alt="Luces aesthetic">
        <p>Luces Aesthetic</p>
      </div>
    </div>
  </div>

  <div id="popup" class="popup">
    <div class="popup-box">¿Qué te importa lo que vendemos?</div>
  </div>

  <script>
    function showMsg(){
      document.getElementById('popup').classList.add('active');
      setTimeout(()=>{
        document.getElementById('popup').classList.remove('active');
      }, 2500);
    }
  </script>
</body>
</html>
