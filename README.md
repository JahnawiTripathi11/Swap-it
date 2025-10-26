# Swapit - Modern Trading Platform

> A full-stack trading platform built with React, Spring Boot, and PostgreSQL

[![React](https://img.shields.io/badge/React-18.3.1-blue)](https://reactjs.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.0-green)](https://spring.io/projects/spring-boot)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-12%2B-blue)](https://www.postgresql.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5.3-blue)](https://www.typescriptlang.org/)

## 🚀 Quick Start

```bash
# 1. Setup database
cd backend
psql -U postgres -f database/init.sql

# 2. Start backend
mvn spring-boot:run

# 3. Start frontend (new terminal)
cd ..
npm install
npm run dev

# 4. Open browser
# http://localhost:5173
```

## 📚 Documentation

| Document | Description |
|----------|-------------|
| **[docs/PROJECT_OVERVIEW.md](docs/PROJECT_OVERVIEW.md)** | 📖 Complete project overview, architecture, and features |
| **[docs/RUNNING_GUIDE.md](docs/RUNNING_GUIDE.md)** | ▶️ How to run the application (frontend + backend) |
| **[docs/setup/BACKEND_SETUP.md](docs/setup/BACKEND_SETUP.md)** | ⚙️ Backend setup and database configuration |
| **[docs/api/API_DOCUMENTATION.md](docs/api/API_DOCUMENTATION.md)** | 📡 Complete API endpoint reference |
| **[docs/guides/INTEGRATION_GUIDE.md](docs/guides/INTEGRATION_GUIDE.md)** | 🔗 Technical integration details |
| **[docs/QUICK_REFERENCE.md](docs/QUICK_REFERENCE.md)** | ⚡ Quick commands and tips |

## 🎯 What is Swapit?

Swapit is a modern trading platform that enables users to:
- 🛍️ Browse and search items in a dynamic marketplace
- 💰 Trade using SWP tokens
- 👤 Manage profiles with reputation scores
- 💳 Track transactions and wallet balance
- 🛒 Add items to shopping cart
- 🏆 Earn achievements through trading

## 🏗️ Tech Stack

### Frontend
- **React 18** + **TypeScript** + **Vite**
- **Tailwind CSS** for styling
- **Framer Motion** for animations
- **JWT** authentication

### Backend
- **Java 17** + **Spring Boot 3.2**
- **Spring Security** + **JWT**
- **Spring Data JPA**
- **PostgreSQL** database
- **Maven** build tool

## ✨ Features

- ✅ User authentication (register/login)
- ✅ Dynamic marketplace with search & filters
- ✅ Shopping cart functionality
- ✅ User profiles with transaction history
- ✅ Wallet with balance tracking
- ✅ Reputation system
- ✅ Real-time data from PostgreSQL
- ✅ Responsive design
- ✅ Secure JWT authentication

## 📦 Project Structure

```
project/
├── backend/              # Spring Boot API
│   ├── src/             # Java source code
│   ├── database/        # SQL scripts
│   └── pom.xml          # Maven config
├── src/                 # React frontend
│   ├── components/      # UI components
│   ├── services/        # API integration
│   ├── context/         # State management
│   └── types/           # TypeScript types
├── README.md            # This file
├── README_PROJECT.md    # Project details
├── README_RUNNING.md    # Running guide
└── package.json         # Node dependencies
```

## 🎬 Getting Started

### Prerequisites
- Java 17+
- Node.js 18+
- PostgreSQL 12+
- Maven 3.6+

### Installation

**1. Clone the repository**
```bash
git clone <repository-url>
cd project
```

**2. Setup database**
```bash
cd backend
psql -U postgres -f database/init.sql
```

**3. Start backend**
```bash
mvn spring-boot:run
```

**4. Start frontend** (new terminal)
```bash
npm install
npm run dev
```

**5. Access the application**
- Frontend: http://localhost:5173
- Backend: http://localhost:8080
- API Health: http://localhost:8080/api/health

For detailed instructions, see **[docs/RUNNING_GUIDE.md](docs/RUNNING_GUIDE.md)**

## 🧪 Testing

### Register a Test User
1. Open http://localhost:5173
2. Click "Sign In" → "Sign up"
3. Create account with:
   - Username: `testuser`
   - Email: `test@example.com`
   - Password: `password123`

### Load Sample Data
```bash
cd backend
psql -U postgres -d swapitdb -f database/sample-data.sql
```

## 📡 API Endpoints

```
Authentication:
POST   /api/auth/register
POST   /api/auth/login

Marketplace:
GET    /api/items/public/available
GET    /api/items/search?keyword=...

Transactions:
GET    /api/transactions/user/{id}
POST   /api/transactions

Cart:
POST   /api/cart/add
GET    /api/cart/user/{id}
```

See **[docs/api/API_DOCUMENTATION.md](docs/api/API_DOCUMENTATION.md)** for complete API reference.

## 🔐 Security

- JWT token-based authentication
- BCrypt password hashing
- CORS configuration
- SQL injection prevention
- Input validation

## 🛠️ Development

### Backend
```bash
cd backend
mvn spring-boot:run    # Start with hot reload
mvn test               # Run tests
mvn clean package      # Build JAR
```

### Frontend
```bash
npm run dev      # Start dev server
npm run build    # Build for production
npm run preview  # Preview build
```

## 📊 Database Schema

- **users** - User accounts and authentication
- **items** - Marketplace listings
- **transactions** - Trade history
- **cart** - Shopping cart items

## 🚢 Deployment

### Backend
```bash
mvn clean package
java -jar target/swapit-backend-1.0.0.jar
```

### Frontend
```bash
npm run build
# Deploy dist/ folder to web server
```

## 📝 Environment Variables

### Backend
`backend/src/main/resources/application.properties`
```properties
server.port=8080
spring.datasource.url=jdbc:postgresql://localhost:5432/swapitdb
spring.datasource.username=swapituser
spring.datasource.password=swapitpass123
```

### Frontend
`.env`
```env
VITE_API_URL=http://localhost:8080/api
```

## 🐛 Troubleshooting

### Backend won't start
- Check PostgreSQL is running
- Verify database credentials
- Ensure port 8080 is free

### Frontend errors
- Run `npm install`
- Check `.env` file exists
- Verify backend is running

See **[docs/RUNNING_GUIDE.md](docs/RUNNING_GUIDE.md)** for detailed troubleshooting.

## 📚 Learn More

- **Project Overview**: [docs/PROJECT_OVERVIEW.md](docs/PROJECT_OVERVIEW.md)
- **Running Guide**: [docs/RUNNING_GUIDE.md](docs/RUNNING_GUIDE.md)
- **Backend Setup**: [docs/setup/BACKEND_SETUP.md](docs/setup/BACKEND_SETUP.md)
- **API Reference**: [docs/api/API_DOCUMENTATION.md](docs/api/API_DOCUMENTATION.md)
- **Integration Details**: [docs/guides/INTEGRATION_GUIDE.md](docs/guides/INTEGRATION_GUIDE.md)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

- Spring Boot for the backend framework
- React team for the frontend library
- PostgreSQL for the database
- Tailwind CSS for styling
- Framer Motion for animations

## 📞 Support

For issues and questions:
- Check the documentation files
- Review troubleshooting sections
- Open an issue on GitHub

---

**Built with ❤️ using React, Spring Boot, and PostgreSQL**

**Version**: 1.0.0 | **Status**: ✅ Running | **Last Updated**: October 2025
