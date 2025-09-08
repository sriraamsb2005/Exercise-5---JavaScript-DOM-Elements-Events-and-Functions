# Exercise-5---JavaScript-DOM-Elements-Events-and-Functions

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Cake Shop</title>
  <link rel="stylesheet" href="cake.css">
</head>
<body>
  <header>
    <h1>CAKE SHOP</h1>
  </header>

  <!-- Cake Images with Price -->
  <section class="cakes">
    <div class="cake">
      <img src="cakerainbox.jpeg" alt="Rainbow Cake">
      <p>Rainbow Cake – Rs. 300</p>
    </div>
    <div class="cake">
      <img src="black.jpg" alt="Chocolate Cake">
      <p>Chocolate Cake – Rs. 200</p>
    </div>
    <div class="cake">
      <img src="red.jpeg" alt="Red Velvet Cake">
      <p>Red Velvet Cake – Rs. 250</p>
    </div>
    <div class="cake">
      <img src="blackforset.JPG" alt="Black Forest Cake">
      <p>Black Forest Cake – Rs. 350</p>
    </div>
  </section>

  <!-- Order Form -->
  <h2>Order Cake</h2>
  <div class="order-box">
    <label>Rainbow Cake (Quantity)</label>
    <input type="number" id="rainbow" value="0"><br><br>

    <label>Chocolate Cake (Quantity)</label>
    <input type="number" id="choco" value="0"><br><br>

    <label>Red Velvet Cake (Quantity)</label>
    <input type="number" id="velvet" value="0"><br><br>

    <label>Black Forest Cake (Quantity)</label>
    <input type="number" id="black" value="0"><br><br>

    <button onclick="placeOrder()">Place Order</button>

    <h3 id="result"></h3>
  </div>



  function placeOrder() {
  let rainbow = parseInt(document.getElementById("rainbow").value) || 0;
  let choco = parseInt(document.getElementById("choco").value) || 0;
  let velvet = parseInt(document.getElementById("velvet").value) || 0;
  let black = parseInt(document.getElementById("black").value) || 0;

  let total = (rainbow * 300) + (choco * 200) + (velvet * 250) + (black * 350);

  if (total > 0) {
    document.getElementById("result").innerHTML =
      "Purchase Order Bill!!! <br> Total Price: Rs. " + total;
  } else {
    document.getElementById("result").innerHTML =
      "Please select at least 1 cake.";
  }
}


  <script src="cake.js"></script>


body {
  font-family: Arial, sans-serif;
  background: #f7f7f7;
  margin: 0;
  padding: 0;
  text-align: center;
}

header {
  background: #b30000;
  color: white;
  padding: 15px;
}

.cakes {
  display: flex;
  justify-content: center;
  margin: 20px;
  gap: 20px;
}

.cake img {
  width: 150px;
  height: 120px;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
}

.cake p {
  margin-top: 5px;
  font-weight: bold;
}

h2 {
  color: #003399;
}

.order-box {
  background: white;
  width: 350px;
  margin: auto;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.2);
  text-align: left;
}

.order-box label {
  font-weight: bold;
}

.order-box input {
  width: 100%;
  padding: 5px;
  margin-top: 5px;
}

.order-box button {
  width: 100%;
  padding: 10px;
  margin-top: 15px;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}

.order-box button:hover {
  background: #0056b3;
}

#result {
  margin-top: 20px;
  color: green;
  font-weight: bold;
  text-align: center;
}

  
</body>
</html>
