# Holstentor CORE

[![License](https://img.shields.io/badge/License-Apache_2.0-D22128?style=for-the-badge&logo=apache)](LICENSE.txt)
[![Language](https://img.shields.io/badge/Language-C%23-239120.svg?style=for-the-badge&logo=csharp)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6.svg?style=for-the-badge&logo=windows)](https://www.microsoft.com/en-us/windows)
[![Framework](https://img.shields.io/badge/.NET-Core%201.1-purple.svg?style=for-the-badge&logo=.net&logoColor=white)](https://dotnet.microsoft.com/apps/aspnet)
[![Database](https://img.shields.io/badge/Database-SQL_Server-005A9C?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)](https://www.microsoft.com/en-us/sql-server)

## 🍽️ Restaurant Management System

A comprehensive restaurant management system built with ASP.NET Core, designed to streamline restaurant operations through an intuitive admin panel. This application focuses on menu management, category organization, gallery management, and internal administration without customer-facing ordering features.

---

## ✨ Features

### 🔐 **User Management**
- User authentication and authorization
- Role-based access control
- Profile management and password changes
- User activity tracking

### 📋 **Menu Management**
- Create, edit, and delete menu items (products)
- Organize products into categories and subcategories
- Product gallery management with image uploads
- Dynamic menu display

### 🗂️ **Category System**
- Multi-level category hierarchy (Categories → Subcategories)
- Category-based product organization
- Easy navigation and filtering

### 🖼️ **Media Management**
- Photo gallery for restaurant ambiance
- Product image galleries
- Header, footer, and about section image management
- Video content support

### 💬 **Communication**
- Internal messaging system
- Message notifications and replies
- Contact form management

### ⚙️ **Administrative Features**
- Comprehensive admin dashboard
- Content management for various sections
- Privacy policy and imprint pages
- Session management

---

## 🛠️ Technology Stack

### **Backend**
- **Framework:** ASP.NET Core 1.1 (.NET Framework 4.6.1)
- **Language:** C#
- **ORM:** Entity Framework Core 1.1.6
- **Authentication:** ASP.NET Core Identity

### **Frontend**
- **UI Framework:** Bootstrap
- **Languages:** HTML5, CSS3, JavaScript
- **Template Engine:** Razor Views (MVC)

### **Database**
- **DBMS:** Microsoft SQL Server
- **Migrations:** Entity Framework Core Migrations

### **Development Tools**
- **IDE:** Visual Studio (recommended)
- **Package Manager:** NuGet
- **Version Control:** Git

---

## 📋 Prerequisites

Before running this project, ensure you have the following installed:

- **Windows OS** (Windows 10 or later recommended)
- **.NET Core SDK 1.1** or compatible version
- **SQL Server** (2016 or later, or SQL Server Express)
- **Visual Studio 2017** or later (or Visual Studio Code with C# extension)
- **IIS Express** (included with Visual Studio)

---

## 🚀 Getting Started

### **1. Clone the Repository**

```bash
git clone https://github.com/yourusername/Holstentor_CORE.git
cd Holstentor_CORE
```

### **2. Configure Database Connection**

Update the connection string in `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=HolstentorDB;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

### **3. Restore NuGet Packages**

```bash
dotnet restore
```

### **4. Apply Database Migrations**

```bash
cd Holstentor
dotnet ef database update
```

### **5. Run the Application**

**Using Visual Studio:**
- Open `Holstentor.sln`
- Press `F5` or click "Start Debugging"

**Using Command Line:**
```bash
cd Holstentor
dotnet run
```

The application will be available at `http://localhost:5000` (or the port specified in your launch settings).

---

## 📁 Project Structure

```
Holstentor_CORE/
├── Holstentor/                 # Main application directory
│   ├── Controllers/            # MVC Controllers
│   ├── Data/                   # Database context and configurations
│   ├── Migrations/             # EF Core migrations
│   ├── Models/                 # Data models and view models
│   ├── Services/               # Business logic and services
│   ├── Views/                  # Razor views
│   │   ├── Admin/              # Admin panel views
│   │   ├── Home/               # Public-facing views
│   │   ├── Profile/            # User profile views
│   │   └── Shared/             # Shared layouts and partials
│   ├── wwwroot/                # Static files (CSS, JS, images)
│   ├── Program.cs              # Application entry point
│   ├── Startup.cs              # Application configuration
│   └── appsettings.json        # Configuration settings
├── LICENSE.txt                 # Apache 2.0 License
└── README.md                   # This file
```

---

## 🔧 Configuration

### **Application Settings**

Configure the application through `appsettings.json`:

- **Connection Strings:** Database connection configuration
- **Logging:** Configure logging levels
- **Application Insights:** Optional telemetry configuration

### **User Secrets**

For sensitive data in development, use the Secret Manager tool:

```bash
dotnet user-secrets set "ConnectionStrings:DefaultConnection" "your-connection-string"
```

---

## 🎯 Usage

### **Admin Panel**

Access the admin panel at `/Admin` after logging in with administrator credentials.

**Key Admin Functions:**
- **Dashboard:** Overview of system status
- **Categories:** Manage menu categories and subcategories
- **Products:** Add, edit, and organize menu items
- **Galleries:** Upload and manage photos and videos
- **Messages:** View and respond to customer inquiries
- **Users:** Manage user accounts and permissions

### **Public Interface**

The public-facing interface allows visitors to:
- Browse the menu by category
- View product details and images
- Explore the restaurant gallery
- Access contact information

---

## 🔐 Security Features

- **Authentication:** Cookie-based authentication with ASP.NET Core Identity
- **Authorization:** Role-based access control for admin features
- **Password Security:** Hashed and salted password storage
- **Session Management:** Secure session handling
- **CSRF Protection:** Built-in anti-forgery token validation

---

## 🧪 Testing

To run tests (if test projects are added):

```bash
dotnet test
```

---

## 🚀 Deployment

### **IIS Deployment**

1. Publish the application:
   ```bash
   dotnet publish -c Release
   ```

2. Configure IIS:
   - Create a new application pool (.NET CLR Version: No Managed Code)
   - Create a new website pointing to the publish folder
   - Ensure the application pool identity has access to the database

3. Update `web.config` with production settings

### **Azure Deployment**

The application can be deployed to Azure App Service with SQL Azure database.

---

## 🛣️ Roadmap

Potential future enhancements:

- [ ] Customer-facing online ordering system
- [ ] Table reservation functionality
- [ ] Multi-language support
- [ ] Mobile application
- [ ] Payment gateway integration
- [ ] Analytics and reporting dashboard
- [ ] Email notification system
- [ ] API for third-party integrations

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 👥 Authors

- **Your Name** - *Initial work*

---

## 🙏 Acknowledgments

- Built with ASP.NET Core
- UI components from Bootstrap
- Icons and assets from various open-source projects

---

## 📝 Changelog

### Version 1.0.0
- Initial release
- Core menu management functionality
- Admin panel implementation
- Gallery management system
- User authentication and authorization

---
*Developed by Amir Argani*
