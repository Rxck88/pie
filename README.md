
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { useState } from "react";

const products = [
  { id: 1, name: "Knot Bracelet (Gold)", price: "50,000₮", image: "/knot-gold.jpg" },
  { id: 2, name: "Knot Bracelet (Silver)", price: "50,000₮", image: "/knot-silver.jpg" },
  { id: 3, name: "Silver Braids Necklace", price: "70,000₮", image: "/silver-braids.jpg" },
  { id: 4, name: "Silver Chain Bracelet", price: "40,000₮", image: "/silver-chain.jpg" },
  { id: 5, name: "Snake Head Necklace (Gold)", price: "45,000₮", image: "/snake-gold.jpg" },
  { id: 6, name: "Snake Head Necklace (Silver)", price: "45,000₮", image: "/snake-silver.jpg" },
  { id: 7, name: "Bosoo Ring (Gold)", price: "12,500₮", image: "/bosoo-gold.jpg" },
  { id: 8, name: "Hevtee Ring (Gold)", price: "12,500₮", image: "/hevtee-gold.jpg" },
  { id: 9, name: "Bosoo Ring (Silver)", price: "12,500₮", image: "/bosoo-silver.jpg" },
  { id: 10, name: "Hevtee Ring (Silver)", price: "12,500₮", image: "/hevtee-silver.jpg" }
];

export default function Home() {
  return (
    <div className="p-6">
      <h1 className="text-3xl font-bold text-center mb-8">LUME Mongolia</h1>
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        {products.map(product => (
          <Card key={product.id}>
            <CardContent className="p-4">
              <img src={product.image} alt={product.name} className="w-full h-48 object-cover mb-4 rounded" />
              <h2 className="text-lg font-semibold mb-2">{product.name}</h2>
              <p className="text-gray-600 mb-2">{product.price}</p>
              <Button className="w-full">Add to Cart</Button>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
