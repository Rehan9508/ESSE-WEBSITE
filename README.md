# 🛒 ESSE Naturals & Nutrition - Full Stack E-Commerce Platform

A modern, production-ready full-stack e-commerce platform for natural health products featuring advanced AI capabilities, voice assistant, real-time chat, payment processing, comprehensive admin panel, and automated content management.

[![Next.js](https://img.shields.io/badge/Next.js-15.4-black.svg)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-18.2-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-blue.svg)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-green.svg)](https://www.python.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.8+-green.svg)](https://www.mongodb.com/)

## 📋 Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Running the Project](#running-the-project)
- [Project Structure](#project-structure)
- [API Documentation](#api-documentation)
- [AI Features](#ai-features)
- [Deployment](#deployment)
- [Contributing](#contributing)

## 🎯 Overview

ESSE Naturals & Nutrition is a comprehensive e-commerce solution built with modern web technologies. It combines a Next.js frontend with a Flask-based AI automation backend, providing a seamless shopping experience with intelligent features like voice shopping, AI-powered recommendations, automated content generation, and real-time chat support.

### Key Highlights

- ✅ **Full Stack Architecture**: Next.js 15 + Flask
- ✅ **AI-Powered**: Google Gemini, Hugging Face BLIP, ML Recommendations
- ✅ **Real-time Features**: Socket.IO chat, live updates
- ✅ **Payment Integration**: Razorpay gateway
- ✅ **Admin Dashboard**: Complete management system
- ✅ **Voice Assistant**: Hindi/English voice interactions
- ✅ **Type-Safe**: Full TypeScript implementation

## 🛠️ Tech Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Next.js** | 15.4.6 | React framework with App Router |
| **React** | 18.2.0 | UI library with hooks |
| **TypeScript** | 5.5.3 | Type safety and better DX |
| **Tailwind CSS** | 3.4.7 | Utility-first styling |
| **Framer Motion** | 10.16.0 | Smooth animations |
| **Radix UI** | Latest | Accessible components |
| **Zustand** | 4.5.2 | State management |
| **Socket.IO Client** | 4.7.2 | Real-time communication |
| **NextAuth.js** | 4.24.11 | Authentication |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | 18+ | Runtime for Next.js API routes |
| **Python** | 3.8+ | AI automation services |
| **Flask** | 3.0.0 | Python web framework |
| **MongoDB** | 6.8+ | NoSQL database |
| **Socket.IO** | 4.7.2 | Real-time server |
| **Razorpay** | 2.9.6 | Payment processing |
| **Twilio** | 5.8.0 | SMS/OTP services |

### AI & ML
| Technology | Version | Purpose |
|------------|---------|---------|
| **Google Gemini** | Latest | Conversational AI, content generation |
| **Hugging Face BLIP** | Latest | Image analysis & captioning |
| **scikit-learn** | 1.3.2 | ML recommendation engine |
| **TensorFlow.js** | 4.12.0 | Client-side ML |
| **Transformers** | 4.36.2 | NLP models |
| **PyTorch** | 2.1.2 | Deep learning framework |

## ✨ Features

### 🛍️ E-Commerce Core
- **Product Catalog**: Advanced filtering, sorting, search
- **Shopping Cart**: Add, remove, update quantities
- **Checkout Process**: Multi-step with address and payment
- **Order Management**: Track orders, order history
- **User Accounts**: Registration, login, profile management
- **Wishlist**: Save products for later
- **Reviews & Ratings**: Customer feedback system

### 🤖 AI-Powered Features
- **Voice Shopping**: "Add turmeric capsules to cart" (Hindi/English)
- **Smart Recommendations**: ML-powered product suggestions
- **AI Chat Support**: Intelligent customer service
- **Content Generation**: Automated product descriptions
- **Image Recognition**: Product identification via camera
- **Voice Search**: Speak to find products

### 👨‍💼 Admin Dashboard
- **Product Management**: CRUD operations, inventory tracking
- **Order Processing**: Order status updates, fulfillment
- **User Management**: Customer data, roles, permissions
- **Analytics**: Sales reports, user behavior, trends
- **Content Management**: Blog posts, pages, SEO
- **Marketing Tools**: Promotions, discounts, campaigns
- **AI Automation**: Automated content generation for products

### 💳 Payment & Security
- **Razorpay Integration**: Cards, UPI, Net Banking, Wallets
- **Secure Checkout**: PCI compliant payment processing
- **Order Tracking**: Real-time status updates
- **Invoice Generation**: Automated billing
- **Refund Management**: Easy refund processing

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** 18+ and npm
- **Python** 3.8+ and pip
- **MongoDB** (local or cloud instance)
- **Git** for version control

### Required API Keys
- Google Gemini API key (free tier available)
- Razorpay keys (for payment processing)
- Twilio credentials (optional, for SMS/OTP)
- Hugging Face token (optional, for higher rate limits)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Rehan9508/ESSE-WEBSITE.git
cd ESSE-WEBSITE/ESSE
```

### 2. Frontend Setup

```bash
# Install Node.js dependencies
npm install

# This will install all Next.js, React, and related dependencies
```

### 3. Backend (AI Automation) Setup

```bash
# Navigate to AI automation directory
cd ai_automation

# Create virtual environment (Windows)
python -m venv ai_env

# Activate virtual environment (Windows)
ai_env\Scripts\activate

# Or on Mac/Linux:
python3 -m venv ai_env
source ai_env/bin/activate

# Install Python dependencies
pip install -r requirements.txt
```

### 4. Environment Configuration

Create a `.env.local` file in the root directory (`ESSE/`):

```env
# Next.js / Frontend Configuration
NEXTAUTH_URL=http://localhost:3005
NEXTAUTH_SECRET=your-nextauth-secret-here-generate-with-openssl-rand-base64-32

# MongoDB Configuration
MONGODB_URI=mongodb://localhost:27017/esse-naturals
# Or for MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/esse-naturals

# Google Gemini AI
GEMINI_API_KEY=your_gemini_api_key_here

# OpenAI (optional)
OPENAI_API_KEY=your_openai_api_key_here

# Payment Gateway - Razorpay
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Twilio (optional, for SMS/OTP)
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_VERIFY_SERVICE_SID=your_twilio_verify_service_sid
```

Create a `.env` file in `ai_automation/` directory:

```env
# Google Gemini API Key
GEMINI_API_KEY=your_gemini_api_key_here

# Hugging Face Token (optional)
HUGGINGFACE_API_TOKEN=your_huggingface_token_here

# Flask Configuration
FLASK_ENV=development
FLASK_DEBUG=True
FLASK_PORT=5000

# Database
DATABASE_URL=sqlite:///ecommerce.db

# Logging
LOG_LEVEL=INFO
LOG_FILE=automation.log
```

### 5. Database Setup

```bash
# Seed the database with sample data
npm run seed          # Products and categories
npm run seed-admin    # Admin users
npm run seed-users    # Sample customers
```

## 🏃 Running the Project

### Development Mode

#### Start Frontend (Next.js)

```bash
# From the ESSE directory
npm run dev
```

The frontend will be available at **http://localhost:3005**

#### Start Backend (AI Automation Flask API)

```bash
# From the ai_automation directory
cd ai_automation
python app.py
```

The AI automation API will be available at **http://127.0.0.1:5000**

#### Start Both Services

Open two terminal windows:

**Terminal 1 - Frontend:**
```bash
cd "C:\Users\Win11\Desktop\ESSE WEBSITE\ESSE"
npm run dev
```

**Terminal 2 - Backend:**
```bash
cd "C:\Users\Win11\Desktop\ESSE WEBSITE\ESSE\ai_automation"
python app.py
```

### Production Build

```bash
# Build Next.js application
npm run build

# Start production server
npm start
```

## 📁 Project Structure

```
ESSE/
├── app/                          # Next.js App Router pages
│   ├── api/                      # API routes
│   │   ├── auth/                 # Authentication endpoints
│   │   ├── products/             # Product management
│   │   ├── orders/               # Order processing
│   │   └── payment/              # Payment gateway integration
│   ├── admin/                    # Admin dashboard pages
│   ├── account/                  # User account pages
│   ├── shop/                     # Shopping pages
│   ├── checkout/                 # Checkout flow
│   └── globals.css               # Global styles
├── components/                    # React components
│   ├── admin/                    # Admin components
│   ├── ai/                       # AI feature components
│   ├── layout/                   # Layout components
│   ├── product/                  # Product components
│   └── ui/                       # Reusable UI components
├── lib/                          # Utility libraries
│   ├── ai/                       # AI service integrations
│   ├── auth.ts                   # Authentication logic
│   ├── mongodb.ts                # Database connection
│   └── razorpay.ts               # Payment integration
├── ai_automation/                 # Python AI backend
│   ├── services/                 # AI service modules
│   │   ├── gemini_service.py    # Google Gemini integration
│   │   ├── blip_service.py      # Hugging Face BLIP
│   │   └── simple_recommendation_service.py  # ML engine
│   ├── app.py                    # Flask API server
│   ├── config.py                 # Configuration
│   └── requirements.txt          # Python dependencies
├── data/                         # Sample data files
├── scripts/                      # Database seeders
├── public/                       # Static assets
├── package.json                  # Node.js dependencies
├── tsconfig.json                 # TypeScript configuration
├── tailwind.config.ts            # Tailwind CSS config
└── README.md                     # This file
```

## 📚 API Documentation

### Frontend API Routes (Next.js)

#### Authentication
```typescript
POST   /api/auth/login          # User login
POST   /api/auth/register       # User registration
GET    /api/auth/session        # Get current session
POST   /api/auth/logout         # User logout
```

#### Products
```typescript
GET    /api/products            # Get all products
GET    /api/products/[id]       # Get single product
POST   /api/products            # Create product (admin)
PUT    /api/products/[id]       # Update product (admin)
DELETE /api/products/[id]       # Delete product (admin)
```

#### Orders
```typescript
POST   /api/orders              # Create new order
GET    /api/orders              # Get user orders
GET    /api/orders/[id]          # Get order details
PUT    /api/orders/[id]          # Update order status
```

#### Payment
```typescript
POST   /api/payment/create-order    # Create Razorpay order
POST   /api/payment/verify          # Verify payment
```

### Backend API Routes (Flask AI Automation)

#### Health Check
```http
GET /health
```

#### Product Content Generation
```http
POST /api/generate-description      # Generate product description
POST /api/generate-categories       # Generate categories and tags
POST /api/generate-seo             # Generate SEO metadata
POST /api/generate-blog            # Generate blog content
POST /api/complete-product-automation  # Full automation pipeline
```

#### Image Analysis
```http
POST /api/analyze-image            # Analyze product image
POST /api/generate-alt-text        # Generate SEO alt text
POST /api/batch-analyze-images    # Batch image processing
```

#### Recommendations
```http
POST /api/train-recommendations    # Train recommendation model
GET  /api/user-recommendations/[user_id]  # Get user recommendations
GET  /api/item-recommendations/[item_id]  # Get similar products
GET  /api/popular-items           # Get popular items
POST /api/predict-rating          # Predict user rating
```

## 🤖 AI Features

### 1. Product Content Generation
Automatically generate product descriptions, SEO metadata, categories, and tags using Google Gemini AI.

### 2. Image Analysis
Analyze product images using Hugging Face BLIP model to generate captions and alt text.

### 3. Recommendation Engine
Machine learning-based product recommendations using collaborative filtering (NMF algorithm).

### 4. Voice Assistant
Voice-powered shopping experience supporting Hindi and English languages.

### 5. AI Chat Support
Intelligent customer support chatbot powered by Google Gemini.

## 🔧 Development Commands

```bash
# Development
npm run dev              # Start Next.js dev server (port 3005)
python ai_automation/app.py  # Start Flask AI API (port 5000)

# Building
npm run build            # Build for production
npm start                # Start production server

# Database
npm run seed             # Seed products and categories
npm run seed-admin       # Seed admin users
npm run seed-users       # Seed sample customers

# Code Quality
npm run lint             # Run ESLint
```

## 🚀 Deployment

### Frontend Deployment (Vercel - Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### Backend Deployment (Python/Flask)

Options:
- **Heroku**: Use `Procfile` and deploy Flask app
- **Railway**: Connect GitHub repo and auto-deploy
- **AWS EC2**: Set up Python environment and run Flask
- **Docker**: Containerize the Flask application

### Environment Variables for Production

Set all environment variables in your hosting platform:
- Vercel: Project Settings → Environment Variables
- Heroku: `heroku config:set KEY=value`
- Railway: Environment Variables tab

### Database (MongoDB Atlas)

1. Create MongoDB Atlas account
2. Create a cluster
3. Get connection string
4. Add to `MONGODB_URI` environment variable
5. Whitelist IP addresses for access

## 🧪 Testing

### Frontend Testing
```bash
# Run linting
npm run lint

# Type checking (implicit in Next.js)
# TypeScript will catch errors during build
```

### Backend Testing
```bash
cd ai_automation
python test_api.py              # Test Flask API endpoints
python manual_test.py           # Test recommendation engine
```

## 📝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow TypeScript best practices
- Use meaningful variable names
- Add comments for complex logic
- Write descriptive commit messages
- Test your changes before pushing

## 🔐 Security

- API keys stored in environment variables (never commit)
- Authentication via NextAuth.js
- Secure payment processing via Razorpay
- Input validation on all forms
- CSRF protection enabled
- Secure headers configured

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Support

- **Documentation**: Check `ai_automation/README.md` for AI backend docs
- **Issues**: Open an issue on GitHub
- **Email**: support@esse-naturals.com (example)

## 🎯 Roadmap

- [ ] Multi-language support
- [ ] Progressive Web App (PWA)
- [ ] Advanced analytics dashboard
- [ ] Mobile app (React Native)
- [ ] Integration with more AI models
- [ ] Advanced recommendation algorithms (Deep Learning)
- [ ] Real-time inventory management
- [ ] Automated marketing campaigns

---

**Built with ❤️ using Next.js, React, TypeScript, Python, and Flask**
