<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

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
