<h1 align="center">
  <img alt="cgapp logo" src="https://raw.githubusercontent.com/CossyCossy/food-delivery/master/html/img/cgapp_logo%402x.png" width="224px"/><br/>
  Food Delivery Backend (Golang + PostgreSQL)
</h1>

<p align="center">
  A production-ready backend system for building a food-delivery platform like <b>Uber Eats</b>, <b>Swiggy</b>, or <b>Glovo</b>.  
  Built with <b>Golang</b>, <b>PostgreSQL</b>, <b>REST APIs</b>, and a scalable backend architecture.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Go-1.18+-00ADD8?style=for-the-badge&logo=go" />
  <img src="https://img.shields.io/badge/PostgreSQL-10.21+-red?style=for-the-badge&logo=postgresql&logoColor=green" />
</p>


---

# 🧐 Project Philosophy

This project provides a **modern, modular, and scalable backend** for a real-world food delivery platform.  
It includes:

- Clean backend architecture using Golang  
- PostgreSQL as the primary database  
- JWT-based authentication  
- APIs for restaurants, menus, cart, orders, and payments  
- Industry-standard project structure  
- Ready-to-use modules similar to Uber Eats, Zomato, and Glovo  

This repository is ideal for learning backend engineering or using it as a foundation for a production project.

---

# 📦 Features

### 🔑 Authentication
- JWT authentication  
- Role-based access (admin, user, restaurant-owner)  
- Secure password hashing  

### 🍽️ Restaurant & Menu
- Add/manage restaurants  
- Add/manage menu items  
- Categories, pricing, availability  

### 🛒 Cart Management
- Add/remove items  
- Cart totals  
- Persisted cart items  

### 📦 Order Management
- Place orders  
- Update order status (pending → accepted → out for delivery → completed)  
- Order history  

### 💳 Payments (Optional)
- Mock payment processing  
- Extendable to Stripe/Razorpay  

### ⚙️ Architecture
- Controllers  
- Models  
- Services  
- Middleware  
- Database migrations  

---

# 🗂️ Database Model

This backend uses PostgreSQL with a clearly defined, normalized schema.

Key tables include:

- **Users** (roles: customer, admin, restaurant-owner)  
- **Restaurants**  
- **Menu Items**  
- **Orders**  
- **Order Items**  
- **Carts**  
- **Payments**  

A detailed database schema is provided in the wiki.

---

# 👨‍💻 Tech Stack

- **Language:** Go (Golang)  
- **Database:** PostgreSQL  
- **ORM / DB Layer:** GORM / pgx  
- **Authentication:** JWT  
- **Router:** Gorilla Mux / Fiber / Gin  
- **Containerization:** Docker (optional)  
- **API Documentation:** Swagger or Postman collection  

---

# 🚀 Getting Started

Below are step-by-step commands and configuration you'll need to run the project locally.

```bash
# 1️⃣ Clone the Repository
git clone https://github.com/your-username/go-food-delivery-backend.git
cd go-food-delivery-backend
```

## 2️⃣ Install Dependencies
```bash
go mod tidy
```

## 3️⃣ Configure Environment Variables
Create a `.env` file in the project root with the following content:
```env
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASS=yourpassword
DB_NAME=fooddelivery
JWT_SECRET=supersecretkey
```

## 4️⃣ Start PostgreSQL (Docker)
```bash
docker run --name fooddb -e POSTGRES_PASSWORD=yourpassword -p 5432:5432 -d postgres
```

## 5️⃣ Run Server
```bash
go run main.go
```

---

## 🧪 Testing
```bash
go test ./...
```

---

## 🐳 Docker Deployment (Optional)
```bash
docker build -t go-food-delivery .
docker run -p 8080:8080 go-food-delivery
```

---

# ✨ Future Improvements

```text
- Redis caching
- API rate limiting
- WebSockets for live order tracking
- Delivery partner module
- CI/CD (GitHub Actions)
- Kubernetes deployment
- More unit/integration tests
```

---

# ✍️ Contributing

```text
Contributions are welcome!
Feel free to open issues or submit pull requests.
```

---

# ⚖️ License

```text
This project is open-source and available under the MIT License.
```

# 🍾 Cheers!

If you like this project, don't forget to ⭐ **star the repository**.  
You’re awesome — keep building!

