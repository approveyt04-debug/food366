<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title><food 36> Menu</title>
  <style>
    body {
      background: #111;
      color: #0f0;
      font-family: 'Courier New', monospace;
      text-align: center;
      padding: 20px;
    }
    h1 {
      color: #0f0;
      text-shadow: 0 0 10px #0f0;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
      gap: 10px;
      margin-top: 20px;
    }
    .food {
      background: #222;
      border: 1px solid #0f0;
      border-radius: 10px;
      padding: 10px;
      transition: 0.3s;
      cursor: pointer;
    }
    .food:hover {
      background: #0f0;
      color: #000;
    }
  </style>
</head>
<body>
  <h1>🍴 &lt;food 36&gt; Menu</h1>
  <div class="grid" id="foodGrid"></div>

  <script>
    const foods = [
      "🍔 Burger", "🍕 Pizza", "🍣 Sushi", "🍜 Ramen", "🍛 Curry", "🥗 Salad",
      "🍤 Shrimp", "🍞 Bread", "🥞 Pancake", "🍩 Donut", "🍦 Ice Cream", "🍖 BBQ",
      "🍗 Fried Chicken", "🌮 Taco", "🌭 Hotdog", "🥪 Sandwich", "🥙 Kebab", "🍚 Rice",
      "🍝 Spaghetti", "🍱 Bento", "🍟 Fries", "🥔 Potato", "🍇 Grapes", "🍉 Watermelon",
      "🍓 Strawberry", "🍍 Pineapple", "🍒 Cherry", "🥭 Mango", "🍎 Apple", "🍌 Banana",
      "🍪 Cookie", "🥧 Pie", "🥯 Bagel", "🧁 Cupcake", "🥮 Mooncake", "🍿 Popcorn"
    ];

    const grid = document.getElementById('foodGrid');
    foods.forEach(food => {
      const div = document.createElement('div');
      div.className = 'food';
      div.textContent = food;
      div.onclick = () => alert(You selected ${food});
      grid.appendChild(div);
    });
  </script>
</body>
</html>
