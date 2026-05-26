import { useState } from "react";

const products = [
  { id: 1, name: "iPhone 15", category: "phones", price: 1000 },
  { id: 2, name: "Samsung Galaxy", category: "phones", price: 900 },
  { id: 3, name: "MacBook Pro", category: "laptops", price: 2000 },
  { id: 4, name: "Lenovo ThinkPad", category: "laptops", price: 1200 },
];

function App() {
  const [search, setSearch] = useState("");
  const [category, setCategory] = useState("all");

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
      <h1>Shop</h1>

      <input
        value={search}
        onChange={(e) => setSearch(e.target.value)}
        placeholder="Search..."
      />

      <select
        value={category}
        onChange={(e) => setCategory(e.target.value)}
      >
        <option value="all">All</option>
        <option value="phones">Phones</option>
        <option value="laptops">Laptops</option>
      </select>

      <div>
        {filteredProducts.map((product) => (
          <div key={product.id}>
            <h3>{product.name}</h3>
            <p>{product.category}</p>
            <p>{product.price}$</p>
          </div>
        ))}
      </div>
    </div>
  );
}

export default App;
