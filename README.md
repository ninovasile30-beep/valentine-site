# valentine-site
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Valentine</title>
<style>
  body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #111;
    color: #fff;
    font-family: Arial, sans-serif;
  }

  .card {
    text-align: center;
  }

  button {
    padding: 12px 24px;
    font-size: 18px;
    margin: 10px;
    cursor: pointer;
    position: relative;
    transition: transform 0.2s;
  }

  #no {
    position: absolute;
  }
</style>
</head>
<body>

<div class="card">
  <h1>Veux-tu être ma Valentine ?</h1>
  <button id="yes">Oui</button>
  <button id="no">Non</button>
</div>

<script>
  const noBtn = document.getElementById("no");
  const yesBtn = document.getElementById("yes");

  noBtn.addEventListener("mouseenter", () => {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  });

  yesBtn.addEventListener("click", () => {
    yesBtn.style.transform = "scale(1.5)";
  });
</script>

</body>
</html>
