function App() {
  const [search, setSearch] = useState("");
  const [category, setCategory] = useState("all");

  // 🔍 ФИЛЬТРАЦИЯ ТОВАРОВ
  const filteredProducts = products.filter((product) => {
    const matchSearch = product.name
      .toLowerCase()
      .includes(search.toLowerCase());

    const matchCategory =
      category === "all" || product.category === category;

    return matchSearch && matchCategory;
  });

  return (
    <div style={{ padding: "20px" }}>
      <h1>🛒 Shop</h1>

      {/* 🔍 SEARCH INPUT */}
      <input
        type="text"
        placeholder="Search products..."
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />

      {/* 📂 CATEGORY FILTER */}
      <select
        value={category}
        onChange={(e) => setCategory(e.target.value)}
      >
        <option value="all">All</option>
        <option value="phones">Phones</option>
        <option value="laptops">Laptops</option>
      </select>

      <hr />

      {/* 🧾 PRODUCTS LIST */}
      {filteredProducts.map((product) => (
        <div
          key={product.id}
          style={{
            border: "1px solid #ccc",
            padding: "10px",
            marginBottom: "10px",
          }}
        >
          <h3>{product.name}</h3>
          <p>Category: {product.category}</p>
          <p>Price: ${product.price}</p>
        </div>
      ))}
    </div>
  );
}

export default App;
