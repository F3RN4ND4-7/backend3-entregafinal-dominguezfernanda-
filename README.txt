# 🧙‍♂️ Proyecto Final Backend 3: El Servidor del Caliz de Fuego 🧙‍♀️

**"Solo aquellos valientes y astutos en las artes oscuras del backend podrán dominar este desafío..."**

Comienza tu viaje con el siguiente hechizo Docker:  
```bash
docker pull fernandadominguez/server-coder:1.0.0
```

---

# 🧙‍♂️ Proyecto Final Backend 2: La Cámara Secreta de APIs 🧙‍♀️

## ⚡ 1. Registra a tu mago (user o admin):
**Usa este encantamiento para invocar un nuevo usuario o administrador en el Mundo Mágico:**

```http
POST localhost:5000/api/auth/register
```

**Mago Usuario:**
```json
{
  "first_name": "user",
  "last_name": "user",
  "email": "user@gmail.com",
  "age": 23,
  "role": "user",
  "password": "1234"
}
```

**Mago Administrador:**
```json
{
  "first_name": "admin",
  "last_name": "admin",
  "email": "admin@gmail.com",
  "age": 23,
  "role": "admin",
  "password": "1234"
}
```

## 🛒 2. Hechizo para crear un producto (solo para administradores):  
```http
POST localhost:5000/api/products
```

```json
{
  "name": "Producto 1",
  "description": "descripcion",
  "price": 100,
  "stock": 10,
  "category": "Bicicleta",
  "image": "a"
}
```

## 🛒 3. Crear un carrito encantado:
```http
POST localhost:5000/api/carts
```

## 🛍️ 4. Agregar productos al carrito:
```http
POST localhost:5000/carts/:idCart/products/:idProd
```

## ✨ 5. Finalizar la compra mágica:
```http
POST localhost:5000/carts/:idCart/purchase
```

```json
{
  "code": "fe85ec73-7c26-446a-b57e-acb06dda7169",
  "purchase_datetime": "2024-08-17T01:48:40.783Z",
  "amount": 500,
  "purchaser": "66bffeee40e9c9729264e6a2",
  "_id": "66c0017840e9c9729264e6f3",
  "__v": 0
}
```

---

# 🧙‍♂️ Pre-entrega del Proyecto Final: "Hechizos Previos" 🧙‍♀️

Primero, asegúrate de instalar los ingredientes mágicos con:
```bash
npm i express mongoose jsonwebtoken passport passport-jwt passport-local bcrypt morgan cookie-parser joi uuidv4 express-session nodemailer twilio
npm run dev
```

## 🔮 Consultar usuarios:
```http
GET localhost:5000/api/users
```

## 📜 Registro de un nuevo mago:
```http
POST localhost:5000/api/auth/register
```
```json
{
    "first_name": "Prueba1",
    "last_name": "Pruebita1",
    "email": "Prueba1@gmail.com",
    "age": 23,
    "role": "admin",
    "password": "1234"
}
```

## 🔑 Autenticación de magos:
```http
POST localhost:5000/api/auth/login
```
```json
{
    "email": "Prueba1@gmail.com",
    "password": "1234"
}
```

## 👤 Consultar el mago autenticado:
```http
GET localhost:5000/api/auth/current
```

---

# 🧙‍♂️ Entrega Final: "El Gran Desafío Backend" 🧙‍♀️

## 🏗️ Crear productos mágicos:
```http
POST localhost:8080/products
```
**Ejemplos de productos encantados:**
```json
{
  "name": "Bicicleta 1",
  "description": "rodado 20",
  "price": 100,
  "thumbnail": "http://imagen_1.jpg",
  "code": "BIKE001",
  "stock": 30
}
```

## 🔍 Obtener productos mágicos:
```http
GET localhost:8080/products
```

## 🔄 Actualizar producto encantado:
```http
PUT localhost:8080/products/:idProd
```

## ❌ Eliminar producto:
```http
DELETE localhost:8080/products/:idProd
```

## 📜 Crear carrito:
```http
POST localhost:8080/carts
```

## 🔮 Obtener carritos:
```http
GET localhost:8080/carts
```

## 🧹 Limpiar carrito:
```http
DELETE localhost:8080/carts/:idCart
```

---

"Este proyecto fue escrito en pergaminos mágicos por fernandadominguez, un maestro en las artes del código oscuro. Que la magia del código te acompañe en tu camino al éxito en el backend. ¡Lumos!"

---