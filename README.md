# BleenGear-Tech-Gaming-Store
A specialized, full-featured e-commerce platform for computer hardware, PC components, and high-performance gaming peripherals. Built with React, Node.js (Express), Python (FastAPI), and MySQL, featuring a cutting-edge Multimodal AI Search Engine (Reverse Image & Semantic Search), real-time hardware configuration, and transactional order management.
## 🚀 Project Overview
BleenGear is a modern e-commerce solution engineered specifically for tech enthusiasts, gamers, and custom PC builders. The platform bridges the gap between visual inspiration and technical specifications by allowing users to search for complex hardware components using real-world setup photos, natural language intent, or hybrid combinations, alongside deep hardware configuration, atomic inventory locking, and instant VietQR banking payments.
## ✨ Key Features

### 🏠 Homepage
- **Hero Showcase** - Interactive presentation of flagship PC builds and performance gear
- **Bento Category Grid** - High-contrast visual navigation for GPUs, Keyboards, Coolers, and Cases
- **Trending Hardware** - Curated carousel featuring real-time specs chips (RTX 4070, 144Hz, Hot-swap)
- **SEO Optimized** - Structured metadata and clean semantic open-graph tags

### 🛍️ E-commerce Core
- **Product Catalog** - Comprehensive hardware browsing with multi-category navigation
- **Advanced Technical Filtering** - Filter by brand, price range, form factor, switch type, and connectivity
- **Instant Search** - Debounced real-time text query suggestions
- **Hardware Details (PDP)** - In-depth product showcases with interactive multi-angle galleries
- **Shopping Cart** - Persistent cart state with dynamic subtotal recalculation
- **Hardware Wishlist** - Save desired components for future builds

### 🧠 Multimodal AI Search Engine
- **Reverse Image Search** - Upload desk setup or component photos to locate matching hardware
- **Semantic Natural Search** - Conversational search understanding natural intent (e.g., *"silent mechanical keyboard for office work"*)
- **Hybrid Multimodal Fusion** - Combine an uploaded image with spec modifiers using weighted vector math ($0.6 \times \text{Image} + 0.4 \times \text{Text}$)
- **Image Cropping Tool** - Built-in canvas cropper to isolate specific peripherals or components from full setup photos
- **Visual Confidence Badges** - Real-time match scoring display on search result cards (e.g., *"94% AI Match"*)
- **Skeleton Shimmer Loading** - Smooth UI feedback during vector embedding extraction

### ⚙️ Hardware Configurator & PDP
- **Multi-Angle Gallery** - High-resolution viewport for close-up port inspects, PCB traces, and backplates
- **Dynamic Variant Matrix** - Select colorways and technical versions (Switch type, RAM/SSD capacities)
- **Live Stock Indicator** - Real-time inventory status badges (e.g., *"In Stock: 8 units left"*)
- **Interactive Price Sync** - Instant price adjustment based on selected hardware configuration
- **Technical Specifications Table** - Structured two-column key-value specification breakdown

### 👤 User Management & Security
- **User Registration** - Account creation with automated welcome flows
- **JWT Authentication** - Secure token-based authentication with Bcrypt password encryption
- **Google OAuth 2.0** - One-click social sign-in integration
- **Inactivity Auto-Logout** - Client-side idle event listeners coupled with server-side session cleanup workers
- **Order History** - Complete purchase tracking and invoice lookup

### 🛒 Checkout & VietQR Banking
- **Transactional Inventory Lock** - Atomic database updates during checkout to eliminate race conditions and over-selling
- **Dynamic VietQR Integration** - Automated QR code generation pre-filled with exact amount, bank account, and order memo
- **Cash on Delivery (COD)** - Traditional doorstep payment option
- **Real-Time Order Tracking** - Visual status pipeline (Pending, Processing, Shipped, Delivered, Cancelled)

### 📊 Store Admin Dashboard
- **KPI Metric Overview** - Real-time statistics for revenue, total orders, and active catalog counts
- **Hardware Inventory Table** - Multi-variant stock tracking with instant edit and deletion controls
- **Multi-Angle Asset Upload** - Direct image upload pipeline integrated with Cloudinary CDN
- **Auto-Vector Sync Trigger** - Automated event hook triggering Python FastAPI to vectorize new hardware upon creation
- **Order Lifecycle Management** - Status updates with automated stock replenishment on cancellation
- **Low-Stock Warnings** - Proactive threshold alerts for components with stock $\le 5$ units

### 📱 Responsive & Cyber Dark Theme
- **Cyberpunk Dark Aesthetic** - Deep slate backgrounds with electric cyber cyan and neon violet accents
- **Mobile-First Responsiveness** - Touch-optimized navigation and configurators across all screen sizes
- **Accessible Typography** - Crisp pairing of Plus Jakarta Sans with JetBrains Mono for specs


## 🛠️ Technologies Used
### Core Frameworks & Runtime
- **React 18** - Component-based client UI library
- **Vite 5** - Next-generation frontend build tooling
- **Node.js 18+** - Asynchronous event-driven JavaScript runtime
- **Express.js 4.19** - Fast, unopinionated backend web framework
- **Python 3.10+** - High-performance runtime for AI microservices
- **FastAPI 0.100+** - Modern, asynchronous Python web API framework
### AI & Computer Vision
- **PyTorch** - Deep learning tensor computation framework
- **Hugging Face Transformers** - Pretrained state-of-the-art vision-language models
- **clip-ViT-B-32-multilingual-v1** - Multimodal vector backbone supporting text and visual embeddings
- **Cosine Similarity Engine** - Vector distance calculation for similarity retrieval
### Database & Asset Management
- **MySQL 8.0 / 9.x** - Relational database with InnoDB engine and native JSON data types
- **mysql2/promise** - High-performance MySQL client with connection pooling
- **Cloudinary SDK** - Cloud asset management for multi-angle hardware photography
### Styling & UI Components
- **Tailwind CSS 3.4** - Utility-first CSS framework
- **Lucide React** - Clean and consistent icon library
- **react-easy-crop** - Canvas-based image cropper for visual search queries
- **Axios** - Promise-based HTTP client
### Authentication & Utilities
- **JSON Web Token (jsonwebtoken)** - Stateless token-based authorization
- **Bcryptjs** - Salted password hashing
- **Google Auth Library** - Google OAuth 2.0 credential verification
- **node-cron** - Task scheduling for inactive session cleanup workers
- **dotenv** - Environment variable management
### Development & Testing Tools
- **Thunder Client / Postman** - API endpoint testing and automation
- **ESLint & Prettier** - Code quality and formatting enforcement
- **Uvicorn** - Lightning-fast ASGI web server for Python
## 📁 Project Structure

<details open>
  <summary><b>Click to expand / collapse Monorepo Directory Architecture</b></summary>
  <br>

  <table>
    <thead>
      <tr>
        <th align="left">Directory / Path</th>
        <th align="left">Architecture Layer</th>
        <th align="left">Scope & Responsibilities</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code><b>frontend/</b></code></td>
        <td><code>React 18 (Vite SPA)</code></td>
        <td>Client-side single-page application and responsive UI layer</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;├── <code>public/</code></td>
        <td><code>Static Assets</code></td>
        <td>Brand logos, payment badges, vector icons, and favicon assets</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;└── <code>src/</code></td>
        <td><code>Application Source</code></td>
        <td>Core React source tree containing components, views, and clients</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>components/</code></td>
        <td><code>UI Component Library</code></td>
        <td>AI search modal, image cropper, PDP variant matrix, VietQR cards</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>pages/</code></td>
        <td><code>Route Views</code></td>
        <td>Home, Catalog, ProductDetail (PDP), Cart, Checkout, AdminDashboard</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <code>services/</code></td>
        <td><code>API Client Layer</code></td>
        <td>Centralized Axios HTTP service modules for backend endpoints</td>
      </tr>
      <tr>
        <td><code><b>backend/</b></code></td>
        <td><code>Node.js (Express.js)</code></td>
        <td>Core web backend, authentication, database pooling, and transactions</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;├── <code>database/</code></td>
        <td><code>Persistence Scripts</code></td>
        <td>Relational schema DDL (MySQL) and realistic hardware seed datasets</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;└── <code>src/</code></td>
        <td><code>Server Runtime</code></td>
        <td>Controllers, middlewares, routes, and asynchronous workers</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>config/</code></td>
        <td><code>System Config</code></td>
        <td>MySQL InnoDB connection pool and Cloudinary storage configuration</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>controllers/</code></td>
        <td><code>Business Logic</code></td>
        <td>Transactional checkout, inventory lock, PDP retrieval, and auth</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>middlewares/</code></td>
        <td><code>Request Interceptors</code></td>
        <td>JWT authentication guards and Multer multi-angle asset parser</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── <code>routes/</code></td>
        <td><code>API Routing</code></td>
        <td>REST endpoint declarations for admin, auth, orders, and products</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── <code>workers/</code></td>
        <td><code>Background Tasks</code></td>
        <td>Scheduled cron jobs executing automatic idle session revocation</td>
      </tr>
      <tr>
        <td><code><b>ai-service/</b></code></td>
        <td><code>Python (FastAPI)</code></td>
        <td>Dedicated microservice for multimodal deep learning vector operations</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;├── <code>main.py</code></td>
        <td><code>FastAPI Endpoints</code></td>
        <td>APIs for image embedding, text embedding, and hybrid search queries</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;├── <code>model.py</code></td>
        <td><code>Model Backbone</code></td>
        <td>Initializes and computes <code>clip-ViT-B-32-multilingual-v1</code> tensors</td>
      </tr>
      <tr>
        <td>&nbsp;&nbsp;└── <code>similarity.py</code></td>
        <td><code>Vector Math</code></td>
        <td>Cosine similarity matching and weighted vector fusion calculations</td>
      </tr>
    </tbody>
  </table>
</details>

🚀 Getting Started
Prerequisites
Node.js v18.0.0 or higher
npm or yarn
Python 3.10 or higher
MySQL Server 8.0 or 9.x

🚀 Deployment
Production Strategy
Frontend: Build static bundle (npm run build) and serve via Nginx or Vercel
Backend: Containerize with Node.js LTS Alpine image and run with PM2 cluster mode
AI Service: Deploy via Docker using Gunicorn with Uvicorn workers
Database: Managed MySQL instance with automated snapshot backups

📄 License
This project is open-source and available under the MIT License.

📞 Support
For questions, bug reports, or feature requests, please open an issue in the repository.
