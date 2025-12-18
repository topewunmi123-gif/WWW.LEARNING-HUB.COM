# WWW.LEARNING-HUB.COM 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Online Store</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f0f8ff;
    }

    header {
      background-color: #0077b6;
      color: white;
      text-align: center;
      padding: 20px;
    }

    nav {
      display: flex;
      justify-content: center;
      background-color: #023e8a;
    }

    nav a {
      color: white;
      text-decoration: none;
      padding: 15px 20px;
      display: block;
    }

    nav a:hover {
      background-color: #0077b6;
    }

    section {
      padding: 50px;
      text-align: center;
    }

    .store {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }

    .product {
      background-color: white;
      width: 200px;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .product:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
    }

    .product img {
      width: 100%;
      border-radius: 10px;
    }

    .product button {
      margin-top: 10px;
      padding: 10px 15px;
      background-color: #0077b6;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }

    .product button:hover {
      background-color: #023e8a;
    }

    #product-detail {
      display: none;
      background-color: #e0f7fa;
      padding: 20px;
      border-radius: 10px;
      margin-top: 20px;
      max-width: 400px;
      margin-left: auto;
      margin-right: auto;
      text-align: left;
    }
  </style>
</head>
<body>

  <header>
    <h1>My Online Store</h1>
    <p>Tap on a product to see details and buy!</p>
  </header>

  <nav>
    <a href="#home">Home</a>
    <a href="#store">Store</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="store">
    <h2>Products</h2>
    <div class="store">
      <div class="product" onclick="showProduct('Ankara Fabric', '₦1800 per yard. High quality Ankara fabric.')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Ankara_fabric.jpg" alt="Ankara">
        <h3>Ankara Fabric</h3>
        <button>Tap to view</button>
      </div>

      <div class="product" onclick="showProduct('Crepe Fabric', '₦1800 per yard. Soft and colorful crepe fabric.')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Crepe_fabric.jpg" alt="Crepe">
        <h3>Crepe Fabric</h3>
        <button>Tap to view</button>
      </div>

      <div class="product" onclick="showProduct('Cotton Fabric', '₦1500 per yard. Comfortable and durable cotton.')">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/5a/Cotton_fabric.jpg" alt="Cotton">
        <h3>Cotton Fabric</h3>
        <button>Tap to view</button>
      </div>
    </div>

    <div id="product-detail"></div>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: shopme@example.com</p>
    <p>WhatsApp: +234 705 524 8780</p>
  </section>

  <script>
    function showProduct(name, description) {
      const detail = document.getElementById('product-detail');
      detail.style.display = 'block';
      detail.innerHTML = `
        <h3>${name}</h3>
        <p>${description}</p>
        <button onclick="buyProduct('${name}')">Buy Now</button>
      `;
      detail.scrollIntoView({ behavior: 'smooth' });
    }

    function buyProduct(name) {
      alert('Thank you! You tapped to buy ' + name + '. Payment can be done via WhatsApp or Opay.');
    }
  </script>

</body>
</html>
