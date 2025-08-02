# نظام المدينة لقطع الغيار - Spare Parts Management System

<div align="center">

![App Logo](public/icon.png)

**A comprehensive spare parts management system built with Electron, React, and MySQL**

[![Electron](https://img.shields.io/badge/Electron-32.0.0-47848F?style=for-the-badge&logo=electron)](https://electronjs.org/)
[![React](https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5.3-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?style=for-the-badge&logo=mysql)](https://www.mysql.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.1-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

</div>

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Development](#development)
- [Building](#building)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

نظام المدينة لقطع الغيار (City Spare Parts System) is a comprehensive desktop application designed for managing spare parts inventory, sales, purchases, and customer relationships. Built as a single executable Electron application, it combines a modern React frontend with an embedded Express.js backend and MySQL database.

### Key Highlights

- 🖥️ **Desktop Application**: Cross-platform Electron app (Windows, macOS, Linux)
- 🎨 **Modern UI**: Beautiful Arabic interface with Tailwind CSS
- 📊 **Real-time Analytics**: Dashboard with charts and reports
- 🏷️ **Barcode Support**: Generate and scan barcodes for products
- 📄 **PDF Generation**: Automatic invoice and report generation
- 🔐 **User Authentication**: Secure login with JWT tokens
- 📱 **Responsive Design**: Works on different screen sizes

## ✨ Features

### 🏪 Inventory Management
- Product catalog with categories and suppliers
- Stock tracking with low stock alerts
- Barcode generation and scanning
- CSV import/export functionality
- Product search with semantic matching

### 💰 Sales & Invoicing
- Fast invoice creation
- Customer management
- Sales history and analytics
- PDF invoice generation
- Returns and refunds handling

### 📦 Purchase Management
- Supplier management
- Purchase orders and receipts
- Cost tracking and profit margins
- Purchase history and reports

### 👥 Customer Management
- Customer database with contact information
- Sales history per customer
- Customer loyalty tracking
- Customer-specific pricing

### 📊 Reporting & Analytics
- Sales reports and charts
- Inventory reports
- Profit/loss analysis
- Export reports to PDF
- Real-time dashboard

### 🔧 System Features
- Multi-language support (Arabic/English)
- User authentication and authorization
- System logs and activity tracking
- Backup and restore functionality
- Settings and configuration management

## 📸 Screenshots

### Dashboard & Analytics
![Dashboard](matrial/Screenshot%202025-08-01%20173826.png)
*Main dashboard with sales analytics and key metrics*

![Analytics](matrial/Screenshot%202025-08-01%20173905.png)
*Detailed analytics and reporting interface*

### Inventory Management
![Inventory](matrial/Screenshot%202025-08-01%20173934.png)
*Product inventory management with search and filtering*

![Product Details](matrial/Screenshot%202025-08-01%20173943.png)
*Product details and stock management*

![Barcode Management](matrial/Screenshot%202025-08-01%20173952.png)
*Barcode generation and management*

### Sales & Invoicing
![Sales](matrial/Screenshot%202025-08-01%20174009.png)
*Sales interface with product selection*

![Invoice](matrial/Screenshot%202025-08-01%20174021.png)
*Invoice creation and management*

![Fast Invoice](matrial/Screenshot%202025-08-01%20174028.png)
*Quick invoice generation interface*

### Customer Management
![Customers](matrial/Screenshot%202025-08-01%20174037.png)
*Customer database and management*

![Customer Details](matrial/Screenshot%202025-08-01%20174043.png)
*Customer information and sales history*

### Purchase Management
![Purchases](matrial/Screenshot%202025-08-01%20174102.png)
*Purchase order management*

![Suppliers](matrial/Screenshot%202025-08-01%20174112.png)
*Supplier management interface*

### Returns & Reports
![Returns](matrial/Screenshot%202025-08-01%20174123.png)
*Returns and refunds management*

![Reports](matrial/Screenshot%202025-08-01%20174131.png)
*Comprehensive reporting system*

### System Features
![Settings](matrial/Screenshot%202025-08-01%20174139.png)
*System settings and configuration*

![System Logs](matrial/Screenshot%202025-08-01%20174150.png)
*System logs and activity tracking*

![AI SQL Generator](matrial/Screenshot%202025-08-01%20174158.png)
*AI-powered SQL query generator with natural language processing*

![AI SQL Generator Interface](matrial/Screenshot%202025-08-01%20181402.png)
*AI SQL Generator interface showing natural language to SQL conversion with connection testing*

![Semantic Search](matrial/Screenshot%202025-08-01%20174206.png)
*Semantic product search functionality*

![Cash Management](matrial/Screenshot%202025-08-01%20174213.png)
*Cash drawer management*

## 🛠️ Technology Stack

### Frontend
- **React 18** - Modern UI framework with hooks
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing
- **React Hook Form** - Form management
- **Recharts** - Data visualization
- **Lucide React** - Icon library

### Backend
- **Express.js** - Web server framework
- **MySQL2** - Database driver
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing
- **Express Validator** - Input validation

### Desktop Application
- **Electron** - Cross-platform desktop framework
- **Electron Builder** - Application packaging
- **Node.js** - Runtime environment

### Additional Libraries
- **jsPDF** - PDF generation
- **bwip-js** - Barcode generation
- **Fuse.js** - Fuzzy search
- **date-fns** - Date manipulation
- **uuid** - Unique identifiers

## 🚀 Installation

### Prerequisites

1. **Node.js** (v16 or higher)
2. **MySQL Server** (v8.0 or higher)
3. **Git** (for cloning the repository)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd electron_version
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure database**
   - Start MySQL server
   - Create a database (or use existing)
   - Update database settings in `electron/config.cjs`

4. **Start development server**
   ```bash
   npm run dev
   ```

### Database Configuration

Edit `electron/config.cjs` to match your MySQL settings:

```javascript
module.exports = {
  database: {
    host: 'localhost',
    user: 'root',
    password: 'your_password',
    database: 'spareparts_erp'
  },
  server: {
    port: 3078,
    jwtSecret: 'your-secret-key'
  }
};
```

## 💻 Usage

### Default Login Credentials
- **Username**: `admin`
- **Password**: `admin123`

### Getting Started

1. **Login** to the application
2. **Configure** your business settings
3. **Add suppliers** and product categories
4. **Import products** or add them manually
5. **Start managing** your inventory and sales

### Key Workflows

#### Adding Products
1. Go to Inventory → Add Product
2. Fill in product details
3. Generate barcode (optional)
4. Set initial stock quantity
5. Save product

#### Creating Sales
1. Go to Sales → New Sale
2. Scan barcode or search products
3. Add customer information
4. Process payment
5. Generate invoice

#### Managing Inventory
1. Monitor stock levels in Dashboard
2. Set up low stock alerts
3. Create purchase orders when needed
4. Update stock quantities
5. Generate inventory reports

## 📚 API Documentation

The application includes a RESTful API with the following endpoints:

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/login-barcode` - Barcode login

### Products
- `GET /api/products` - Get products with pagination
- `GET /api/products/all` - Get all products
- `POST /api/products` - Create new product
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product

### Sales
- `GET /api/sales` - Get sales history
- `POST /api/sales` - Create new sale
- `GET /api/sales/:id` - Get sale details

### Customers
- `GET /api/customers` - Get customers
- `POST /api/customers` - Create customer
- `PUT /api/customers/:id` - Update customer

### Invoices
- `GET /api/invoices` - Get invoices
- `POST /api/invoices` - Create invoice
- `GET /api/invoices/:id/pdf` - Generate PDF

## 🛠️ Development

### Project Structure
```
electron_version/
├── electron/              # Electron main process
│   ├── main.cjs          # Main process
│   ├── server.cjs        # Embedded Express server
│   ├── config.cjs        # Configuration
│   └── preload.js        # Preload script
├── src/                  # React frontend
│   ├── components/       # React components
│   ├── pages/           # Page components
│   ├── services/        # API services
│   ├── contexts/        # React contexts
│   └── utils/           # Utility functions
├── server/              # Original server (reference)
├── public/              # Static assets
└── release/             # Built application
```

### Development Commands

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Build Electron app
npm run build:electron

# Build for specific platforms
npm run build:win    # Windows
npm run build:mac    # macOS
npm run build:linux  # Linux

# Run tests
npm run test:merged

# Lint code
npm run lint
```

### Code Style

The project uses:
- **ESLint** for code linting
- **TypeScript** for type safety
- **Prettier** for code formatting
- **Tailwind CSS** for styling

## 📦 Building

### For Distribution

1. **Build the application**
   ```bash
   npm run build:win    # Windows
   npm run build:mac    # macOS
   npm run build:linux  # Linux
   ```

2. **Find the executable**
   - Windows: `release/نظام المدينة لقطع الغيار Setup 1.0.0.exe`
   - macOS: `release/نظام المدينة لقطع الغيار-1.0.0.dmg`
   - Linux: `release/نظام المدينة لقطع الغيار-1.0.0.AppImage`

### Build Configuration

The build configuration is in `package.json`:

```json
{
  "build": {
    "appId": "com.yourcompany.electronapp",
    "productName": "نظام المدينة لقطع الغيار",
    "directories": {
      "output": "release"
    },
    "files": [
      "dist/**/*",
      "electron/**/*",
      "server/**/*",
      "package.json"
    ]
  }
}
```

## 🔧 Troubleshooting

### Common Issues

#### Database Connection
- Ensure MySQL server is running
- Check database credentials in `electron/config.cjs`
- Verify database user permissions

#### Port Conflicts
If port 3078 is in use, change it in `electron/config.cjs`:
```javascript
server: {
  port: 3079  // Use different port
}
```

#### Build Issues
- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Update Electron dependencies: `npm update`
- Check for platform-specific requirements

#### Application Won't Start
- Check console logs for error messages
- Ensure all dependencies are installed
- Try running in development mode first

### Logs

Application logs are stored in:
- **Development**: Console output
- **Production**: Application data directory
- **Database**: MySQL error logs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes
4. Test thoroughly
5. Commit your changes: `git commit -m 'Add feature'`
6. Push to the branch: `git push origin feature-name`
7. Submit a pull request

### Development Guidelines

- Follow TypeScript best practices
- Use meaningful commit messages
- Test on multiple platforms
- Update documentation as needed
- Follow the existing code style

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Electron** team for the desktop framework
- **React** team for the UI library
- **Tailwind CSS** for the styling framework
- **MySQL** for the database system
- All contributors and users of this application

## 📞 Support

For support and questions:
- Create an issue in the repository
- Check the troubleshooting section
- Review the documentation
- Contact the development team

---

<div align="center">

**نظام المدينة لقطع الغيار** - Empowering spare parts businesses with modern technology

Built with ❤️ using Electron, React, and MySQL

</div>