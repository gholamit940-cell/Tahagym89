<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>فروشگاه مکمل ورزشی</title>
<style>
body {
    font-family: sans-serif;
    margin: 0;
    background: #111;
    color: white;
}

header {
    background: #000;
    padding: 15px;
    text-align: center;
    font-size: 22px;
    font-weight: bold;
}

.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

.card {
    background: #1e1e1e;
    padding: 15px;
    border-radius: 10px;
    text-align: center;
}

.card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
}

.price {
    color: #00ff88;
    margin: 10px 0;
}

button {
    background: #00ff88;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    font-weight: bold;
    border-radius: 5px;
}

button:hover {
    opacity: 0.8;
}

#cart {
    position: fixed;
    bottom: 0;
    width: 100%;
    background: #000;
    padding: 10px;
    text-align: center;
}
</style>
</head>
<body>

<header> فروشگاه مکمل ورزشی </header>

<div class="container">

<div class="card">
    <img src="https://via.placeholder.com/300x200" alt="">
    <h3>پروتئین وی</h3>
    <div class="price">1,200,000 تومان</div>
    <button onclick="addToCart('پروتئین وی',1200000)">افزودن به سبد</button>
</div>

<div class="card">
    <img src="https://via.placeholder.com/300x200" alt="">
    <h3>کراتین مونوهیدرات</h3>
    <div class="price">650,000 تومان</div>
    <button onclick="addToCart('کراتین',650000)">افزودن به سبد</button>
</div>

<div class="card">
    <img src="https://via.placeholder.com/300x200" alt="">
    <h3>گینر حجم</h3>
    <div class="price">1,800,000 تومان</div>
    <button onclick="addToCart('گینر',1800000)">افزودن به سبد</button>
</div>

</div>

<div id="cart">
    سبد خرید: <span id="cart-count">0</span> محصول |
    مجموع: <span id="total">0</span> تومان
</div>

<script>
let count = 0;
let total = 0;

function addToCart(name, price) {
    count++;
    total += price;
    document.getElementById("cart-count").innerText = count;
    document.getElementById("total").innerText = total.toLocaleString();
}
</script>

</body>
</html>
