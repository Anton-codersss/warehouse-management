# Warehouse Management System
## Система управления складским комплексом

A complete client-server application for warehouse complex maintenance designed for exploitation engineers.

## 🏗️ **Architecture**
- **Frontend**: React + Vite (running on http://localhost:5176)
- **Backend**: Node.js + Express (running on http://localhost:5000)
- **Database**: PostgreSQL (with mock data fallback)

## 🚀 **Quick Start**

### Prerequisites
- Node.js (v16 or higher)
- PostgreSQL (optional - app works with mock data)

### Running the Application

1. **Start Backend Server**
   ```bash
   cd warehouse-backend
   npm run dev
   ```
   Server will run on http://localhost:5000

2. **Start Frontend Server**
   ```bash
   cd warehouse-frontend
   npm run dev
   ```
   Frontend will run on http://localhost:5176

3. **Access the Application**
   Open http://localhost:5176 in your browser

## 📊 **Features - 9 Warehouse Modules**

1. **🏭 Складское Оборудование** - Warehouse Equipment Management
2. **🚛 Складская Техника** - Warehouse Machinery Management  
3. **🐛 ПЕСТ Контроль** - Pest Control Management
4. **⚡ Энергоресурсы** - Energy Resources Monitoring
5. **🚨 Аварийные ситуации** - Emergency Situations Management
6. **🔧 Работы** - Work Orders and Maintenance
7. **📋 Схемы** - Technical Schemes and Drawings
8. **📦 Расходные материалы** - Consumables Inventory
9. **♻️ Вторичное сырье** - Secondary Materials Management

## 🗄️ **Database Setup (Optional)**

If you want to use PostgreSQL instead of mock data:

1. Install PostgreSQL
2. Create database: `warehouse_management`
3. Run the schema: `warehouse-backend/database/schema.sql`
4. Update credentials in `warehouse-backend/.env`

## 🔧 **Environment Configuration**

Backend environment variables (`.env`):
```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=warehouse_management
DB_USER=postgres
DB_PASSWORD=password
PORT=5000
FRONTEND_URL=http://localhost:5176
```

## 📁 **Project Structure**

```
warehouse-backend/
├── server.js              # Main server file
├── config/database.js     # Database configuration
├── routes/                # API routes for all modules
├── data/mockData.js       # Mock data for demonstration
└── database/schema.sql    # PostgreSQL schema

warehouse-frontend/
├── src/
│   ├── components/        # React components for each module
│   ├── services/api.js    # API service layer
│   └── App.jsx           # Main application component
└── public/
```

## 🎯 **API Endpoints**

All endpoints are available at `http://localhost:5000/api/`:

- `/equipment` - Equipment management
- `/machinery` - Machinery management
- `/pest-control` - Pest control records
- `/energy-resources` - Energy resource monitoring
- `/emergency` - Emergency situations
- `/works` - Work orders
- `/schemes` - Technical schemes
- `/consumables` - Consumables inventory
- `/secondary-materials` - Secondary materials

## 🔄 **Current Status**

✅ **Working Features:**
- Complete dashboard with 9 modules
- Equipment management with mock data
- Machinery management with mock data
- Consumables inventory with mock data
- Responsive design
- API integration

🚧 **In Development:**
- Full CRUD operations for all modules
- Database integration
- File upload for schemes
- Advanced filtering and search

## 📝 **Notes**

- Application currently uses mock data when PostgreSQL is not available
- All modules have basic structure implemented
- Equipment, Machinery, and Consumables modules have working data display
- Other modules show placeholder content and are ready for development