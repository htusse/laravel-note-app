# Laravel Sample Application

A modern Laravel application demonstrating user authentication, note management, and profile management features. Built with Laravel 12, Tailwind CSS, and Alpine.js.

## 🚀 Features

- **User Authentication**: Complete authentication system with registration, login, password reset, and email verification
- **Note Management**: CRUD operations for personal notes with user-specific data
- **Profile Management**: User profile editing and account management
- **Modern UI**: Beautiful, responsive interface built with Tailwind CSS
- **Real-time Development**: Hot reloading with Vite and concurrent development servers

## 🛠️ Tech Stack

- **Backend**: Laravel 12 (PHP 8.2+)
- **Frontend**: Tailwind CSS, Alpine.js
- **Build Tool**: Vite
- **Database**: SQLite (default), supports MySQL/PostgreSQL
- **Testing**: Pest PHP
- **Authentication**: Laravel Breeze

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- PHP 8.2 or higher
- Composer
- Node.js (for frontend assets)
- Git

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/htusse/laravel-note-app.git
   cd laravel-sample-app
   ```

2. **Install PHP dependencies**
   ```bash
   composer install
   ```

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

4. **Environment setup**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Database setup**
   ```bash
   # For SQLite (default)
   touch database/database.sqlite
   
   # Or configure your preferred database in .env
   # DB_CONNECTION=mysql
   # DB_HOST=127.0.0.1
   # DB_PORT=3306
   # DB_DATABASE=laravel_sample_app
   # DB_USERNAME=root
   # DB_PASSWORD=
   ```

6. **Run migrations**
   ```bash
   php artisan migrate
   ```

7. **Seed the database (optional)**
   ```bash
   php artisan db:seed
   ```

## 🏃‍♂️ Running the Application

### Development Mode

For the best development experience, use the concurrent development script:

```bash
composer run dev
```

This command starts:
- Laravel development server
- Queue listener
- Log viewer (Pail)
- Vite development server

### Manual Setup

Alternatively, you can run services individually:

1. **Start Laravel server**
   ```bash
   php artisan serve
   ```

2. **Build frontend assets**
   ```bash
   npm run dev
   ```

3. **Start queue worker (if using queues)**
   ```bash
   php artisan queue:work
   ```

The application will be available at `http://localhost:8000`

## 📁 Project Structure

```
laravel-sample-app/
├── app/
│   ├── Http/Controllers/     # Application controllers
│   ├── Models/              # Eloquent models
│   └── View/Components/     # Blade components
├── database/
│   ├── migrations/          # Database migrations
│   ├── seeders/            # Database seeders
│   └── factories/          # Model factories
├── resources/
│   ├── views/              # Blade templates
│   ├── css/               # Stylesheets
│   └── js/                # JavaScript files
├── routes/                 # Application routes
└── tests/                 # Application tests
```

## 🔐 Authentication

The application includes a complete authentication system:

- **Registration**: User registration with email verification
- **Login**: Secure login with remember me functionality
- **Password Reset**: Email-based password reset
- **Email Verification**: Email verification for new accounts
- **Profile Management**: User profile editing and account deletion

## 📝 Note Management

Users can manage their personal notes:

- **Create**: Add new notes with rich text content
- **Read**: View all notes with pagination
- **Update**: Edit existing notes
- **Delete**: Remove notes from the system

Each note is associated with the authenticated user, ensuring data privacy.

## 🧪 Testing

Run the test suite using:

```bash
composer test
```

Or run tests individually:

```bash
php artisan test
```

## 🛠️ Development Commands

```bash
# Clear application cache
php artisan cache:clear

# Clear configuration cache
php artisan config:clear

# Clear route cache
php artisan route:clear

# Clear view cache
php artisan view:clear

# Run database migrations
php artisan migrate

# Rollback migrations
php artisan migrate:rollback

# Create a new migration
php artisan make:migration create_table_name

# Create a new controller
php artisan make:controller ControllerName

# Create a new model
php artisan make:model ModelName

# Start Tinker (Laravel REPL)
php artisan tinker
```

## 📦 Available Scripts

- `composer dev` - Start all development servers concurrently
- `composer test` - Run the test suite
- `npm run dev` - Start Vite development server
- `npm run build` - Build production assets

## 🔧 Configuration

Key configuration files:

- `.env` - Environment variables
- `config/app.php` - Application configuration
- `config/database.php` - Database configuration
- `config/auth.php` - Authentication configuration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Laravel documentation](https://laravel.com/docs)
2. Review the application logs in `storage/logs/`
3. Ensure all dependencies are properly installed
4. Verify your environment configuration

## 🎯 Next Steps

Potential enhancements for this application:

- Add note categories/tags
- Implement note sharing between users
- Add file attachments to notes
- Implement real-time notifications
- Add API endpoints for mobile applications
- Implement note search functionality
- Add note export features (PDF, Markdown)

---

**Happy coding! 🚀**
