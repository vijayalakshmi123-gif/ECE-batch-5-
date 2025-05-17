Source code: 
-# Simple personalized email generator
def generate_email(customer):
    name = customer.get("name", "Customer")
    product = customer.get("recommended_product", "our latest items")
    
    email = f"""
    Hi {name},

    We thought you'd love to hear about {product}.
    Based on your recent activity, it's a perfect match for you!

    Click here to check it out: https://example.com/products/{product.replace(' ', '-').lower()}
    
    Best,
    Your Company Team
    """
    return email

# Example customer data
customer_data = {
    "name": "Alice",
    "recommended_product": "Wireless Earbuds"
}

print(generate_email(customer_data))
