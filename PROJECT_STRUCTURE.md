# Project Structure

Complete folder structure of the Swapit trading platform.

## 📁 Root Directory

```
project/
├── README.md                     # Main project README
├── PROJECT_STRUCTURE.md          # This file
├── package.json                  # Frontend dependencies
├── vite.config.ts                # Vite configuration
├── tailwind.config.js            # Tailwind CSS config
├── tsconfig.json                 # TypeScript config
├── .env                          # Environment variables
├── .env.example                  # Environment template
├── .gitignore                    # Git ignore rules
│
├── docs/                         # 📚 Documentation
│   ├── README.md                 # Documentation index
│   ├── PROJECT_OVERVIEW.md       # Project details
│   ├── RUNNING_GUIDE.md          # Running instructions
│   ├── QUICK_REFERENCE.md        # Quick reference
│   ├── DOCUMENTATION_INDEX.md    # Full documentation index
│   │
│   ├── setup/                    # Setup guides
│   │   └── BACKEND_SETUP.md      # Backend setup guide
│   │
│   ├── guides/                   # Development guides
│   │   ├── INTEGRATION_GUIDE.md  # Integration details
│   │   └── INTEGRATION_SUMMARY.md# Integration overview
│   │
│   └── api/                      # API documentation
│       └── API_DOCUMENTATION.md  # Complete API reference
│
├── scripts/                      # 🔧 Utility scripts
│   ├── run-project.bat           # Start both frontend & backend
│   ├── run-backend.bat           # Start backend only
│   └── setup-database.bat        # Database setup script
│
├── backend/                      # ☕ Java Spring Boot Backend
│   ├── src/
│   │   └── main/
│   │       ├── java/com/swapit/
│   │       │   ├── SwapitApplication.java
│   │       │   │
│   │       │   ├── controller/   # REST API endpoints
│   │       │   │   ├── AuthController.java
│   │       │   │   ├── UserController.java
│   │       │   │   ├── ItemController.java
│   │       │   │   ├── TransactionController.java
│   │       │   │   ├── CartController.java
│   │       │   │   └── HealthController.java
│   │       │   │
│   │       │   ├── service/      # Business logic
│   │       │   │   ├── UserService.java
│   │       │   │   ├── ItemService.java
│   │       │   │   ├── TransactionService.java
│   │       │   │   └── CartService.java
│   │       │   │
│   │       │   ├── repository/   # Data access layer
│   │       │   │   ├── UserRepository.java
│   │       │   │   ├── ItemRepository.java
│   │       │   │   ├── TransactionRepository.java
│   │       │   │   └── CartRepository.java
│   │       │   │
│   │       │   ├── entity/       # JPA entities
│   │       │   │   ├── User.java
│   │       │   │   ├── Item.java
│   │       │   │   ├── Transaction.java
│   │       │   │   └── Cart.java
│   │       │   │
│   │       │   ├── dto/          # Data transfer objects
│   │       │   │   ├── UserDTO.java
│   │       │   │   ├── ItemDTO.java
│   │       │   │   ├── TransactionDTO.java
│   │       │   │   ├── CartDTO.java
│   │       │   │   ├── AuthRequest.java
│   │       │   │   ├── AuthResponse.java
│   │       │   │   └── RegisterRequest.java
│   │       │   │
│   │       │   └── security/     # Security configuration
│   │       │       ├── JwtUtil.java
│   │       │       ├── JwtAuthenticationFilter.java
│   │       │       ├── SecurityConfig.java
│   │       │       └── UserDetailsServiceImpl.java
│   │       │
│   │       └── resources/
│   │           └── application.properties
│   │
│   ├── database/                 # Database scripts
│   │   ├── init.sql              # Database initialization
│   │   └── sample-data.sql       # Test data
│   │
│   ├── pom.xml                   # Maven dependencies
│   ├── README.md                 # Backend README
│   └── .gitignore                # Backend git ignore
│
└── src/                          # ⚛️ React Frontend
    ├── components/               # React components
    │   ├── Navigation.tsx
    │   ├── NavigationIntegrated.tsx
    │   ├── Hero.tsx
    │   ├── SignUpVerification.tsx
    │   ├── Marketplace.tsx
    │   ├── MarketplaceIntegrated.tsx
    │   ├── Gamification.tsx
    │   ├── Wallet.tsx
    │   ├── WalletIntegrated.tsx
    │   ├── ChatCommunity.tsx
    │   ├── Profile.tsx
    │   ├── ProfileIntegrated.tsx
    │   ├── SwapitAI.tsx
    │   ├── UserChat.tsx
    │   └── AuthModal.tsx
    │
    ├── context/                  # React Context
    │   └── AuthContext.tsx       # Authentication state
    │
    ├── services/                 # API integration
    │   ├── api.ts                # Base HTTP client
    │   ├── authService.ts        # Auth operations
    │   ├── itemService.ts        # Item operations
    │   ├── transactionService.ts # Transaction operations
    │   └── cartService.ts        # Cart operations
    │
    ├── types/                    # TypeScript types
    │   └── index.ts              # Type definitions
    │
    ├── config/                   # Configuration
    │   └── api.ts                # API endpoints config
    │
    ├── App.tsx                   # Main app component
    ├── main.tsx                  # Entry point
    └── index.css                 # Global styles
```

## 📊 Statistics

### Backend
- **Controllers**: 6 files
- **Services**: 4 files
- **Repositories**: 4 files
- **Entities**: 4 files
- **DTOs**: 7 files
- **Security**: 4 files
- **Total Java Files**: ~30 files
- **Lines of Code**: ~3,500 lines

### Frontend
- **Components**: 15 files
- **Services**: 5 files
- **Context**: 1 file
- **Types**: 1 file
- **Total TypeScript Files**: ~22 files
- **Lines of Code**: ~2,000 lines

### Documentation
- **Main Docs**: 4 files
- **Setup Guides**: 1 file
- **Development Guides**: 2 files
- **API Docs**: 1 file
- **Total Documentation**: 8 files

### Scripts
- **Utility Scripts**: 3 files

## 🎯 Key Directories

### `/docs`
All project documentation organized by category:
- Setup guides
- Running instructions
- API reference
- Integration guides

### `/scripts`
Utility scripts for:
- Starting the project
- Database setup
- Backend management

### `/backend`
Java Spring Boot application:
- REST API endpoints
- Business logic
- Database access
- Security configuration

### `/src`
React frontend application:
- UI components
- API integration
- State management
- Type definitions

## 📝 Important Files

### Configuration Files
- `package.json` - Frontend dependencies
- `backend/pom.xml` - Backend dependencies
- `.env` - Environment variables
- `vite.config.ts` - Vite configuration
- `tailwind.config.js` - Tailwind CSS
- `tsconfig.json` - TypeScript config
- `backend/src/main/resources/application.properties` - Backend config

### Entry Points
- `src/main.tsx` - Frontend entry point
- `backend/src/main/java/com/swapit/SwapitApplication.java` - Backend entry point

### Database
- `backend/database/init.sql` - Database schema
- `backend/database/sample-data.sql` - Test data

## 🔍 Finding Files

### I need to...

**...modify the API**
→ `backend/src/main/java/com/swapit/controller/`

**...change business logic**
→ `backend/src/main/java/com/swapit/service/`

**...update database schema**
→ `backend/database/init.sql`

**...modify UI components**
→ `src/components/`

**...change API integration**
→ `src/services/`

**...update authentication**
→ `src/context/AuthContext.tsx` (frontend)
→ `backend/src/main/java/com/swapit/security/` (backend)

**...configure the app**
→ `.env` (frontend)
→ `backend/src/main/resources/application.properties` (backend)

**...read documentation**
→ `docs/`

**...run scripts**
→ `scripts/`

## 🎨 Code Organization

### Backend (Layered Architecture)
```
Controller → Service → Repository → Database
```

### Frontend (Component-Based)
```
Components → Services → API → Backend
```

### Data Flow
```
User → Frontend → API Service → Backend Controller → Service → Repository → Database
```

## 📦 Dependencies

### Frontend
- React ecosystem
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Lucide Icons

### Backend
- Spring Boot
- Spring Security
- Spring Data JPA
- PostgreSQL Driver
- JWT libraries
- Lombok

## 🚀 Quick Navigation

- **Main README**: [README.md](README.md)
- **Documentation**: [docs/](docs/)
- **Backend Code**: [backend/src/main/java/com/swapit/](backend/src/main/java/com/swapit/)
- **Frontend Code**: [src/](src/)
- **Scripts**: [scripts/](scripts/)
- **Database**: [backend/database/](backend/database/)

---

**Last Updated**: October 2025

**Version**: 1.0.0
