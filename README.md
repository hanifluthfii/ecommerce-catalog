# E-Commerce Catalog (Vue.js)

Project ini dibuat sebagai Final Task VIX Core Initiative – Frontend Developer.
Aplikasi menampilkan katalog produk dari FakeStoreAPI dan mengimplementasikan desain Figma menggunakan Vue.js + Vanilla CSS.

---

## 🏷 Tech Stack & Tools

![Vue](https://img.shields.io/badge/Vue.js-2.x-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS](https://img.shields.io/badge/CSS-Vanilla-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![API](https://img.shields.io/badge/FakeStoreAPI-REST-FF9900?style=for-the-badge)
![Git](https://img.shields.io/badge/Git-Version--Control-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)

---

## 🚀 Features
- Fetch data produk dari FakeStoreAPI
- Menampilkan produk kategori:
  - men's clothing  
  - women's clothing  
- Jika kategori tidak sesuai → tampilkan halaman "Unavailable Product"
- Tombol Next Product untuk ganti produk (loop 1–20)
- Halaman berubah sesuai kategori (men / women / unavailable)
- CSS sesuai Figma (tanpa framework)

---

## 🎨 Halaman yang tersedia
- **Men Section**
- **Women Section**
- **Unavailable Product Section**

---

## 📡 API Endpoint

Semua produk diambil dari:

https://fakestoreapi.com/products/:id](https://fakestoreapi.com/docs


ID berjalan **1 → 20**, lalu kembali ke **1**.

---

## 🔧 Cara Menjalankan Project

### 1. Clone Repository
git clone https://github.com/hanifluthfii/ecommerce-catalog.git

### 2. Masuk ke folder project
cd ecommerce-catalog

### 3. Install dependencies
npm install

### 4. Jalankan aplikasi
npm run serve

---

## 🧠 Cara Kerja Next Product
1. User klik tombol **Next Product**
2. index bertambah 1  
3. fetch data berdasarkan ID  
4. Jika category =  
   - men's clothing → tampilkan Men UI  
   - women's clothing → tampilkan Women UI  
   - lainnya → tampilkan Unavailable UI  
5. Jika index = 20 → balik ke 1

---

## 📁 Struktur Project
```
src/
 ├─ assets/
 │   ├─ bg-pattern.svg
 │   ├─ bg-pattern-1.svg
 │   ├─ sad-face.png
 │   └─ style.css
 ├─ components/
 │   ├─ ProductCard.vue
 │   └─ UnavailableProduct.vue
 ├─ App.vue
 ├─ main.js
 └─ ...
```


---

## 👤 Author
**Hanif Luthfi Irfanudin**  
VIX Core Initiative – Frontend Developer

---

## 📌 Repository
https://github.com/hanifluthfii/ecommerce-catalog
