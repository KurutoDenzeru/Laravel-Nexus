# Laravel Nexus

Modern task management app powered by a Laravel backend and a React frontend. Styled with TailwindCSS + DaisyUI for a clean, responsive experience.

## 🚀 Features

- **Task Management**: Create, view, mark as done, and delete tasks
- **Modern UI**: React frontend with TailwindCSS and DaisyUI components
- **API-Driven**: RESTful API endpoints for seamless data operations
- **Real-time Updates**: Dynamic task list updates without page refresh
- **Responsive Design**: Coffee theme with mobile-friendly interface

## 🛠️ Tech Stack

- **Backend**: Laravel 11, PHP 8.2+
- **Frontend**: React 19, TypeScript
- **Styling**: TailwindCSS, DaisyUI
- **Build Tool**: Vite
- **Database**: SQLite (configurable)

## 📁 Project Structure

```
Laravel-Nexus/
├── app/
│   ├── Http/Controllers/Api/TaskApiController.php
│   └── Models/Task.php
├── resources/
│   ├── js/components/
│   │   ├── views/
│   │   ├── context/TaskContext.tsx
│   │   └── services/apiService.ts
│   └── views/app.blade.php
├── routes/
│   ├── api.php
│   └── web.php
└── database/migrations/
```

## 🔧 Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd Laravel-Nexus
   ```

2. **Install PHP dependencies**

   ```bash
   composer install
   ```

3. **Install Node.js dependencies**

   ```bash
   bun install
   ```

4. **Environment setup**

   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Database setup**

   ```bash
   touch database/database.sqlite
   php artisan migrate
   ```

6. **Build assets**

   ```bash
   npm run build
   ```

## 🚀 Development

1. **Start the Laravel server**

   ```bash
   php artisan serve
   ```

2. **Start Vite development server**

   ```bash
   npm run dev
   ```

3. **Access the application**
   - Frontend: `http://localhost:8000`
   - API Base: `http://localhost:8000/api`

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/save-task` | Create a new task |
| GET | `/api/get-task-list` | Retrieve all incomplete tasks |
| PUT | `/api/mark-as-done/{id}` | Mark task as completed |
| DELETE | `/api/delete-task/{id}` | Delete a task |

## 🧪 Testing

```bash
# Run PHP tests
php artisan test

# Run specific test
php artisan test tests/Feature/ExampleTest.php
```

## 🎨 Customization

- **Theme**: Modify DaisyUI theme in `tailwind.config.js`
- **Styling**: Update TailwindCSS classes in React components
- **API**: Extend endpoints in `routes/api.php` and `TaskApiController`

## 📝 Environment Variables

```env
APP_NAME=Laravel-Nexus
APP_URL=http://localhost:8000
API_BASE_URL=http://localhost:8000/api
DB_CONNECTION=sqlite
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Built With

- [Laravel](https://laravel.com) - PHP Framework
- [React](https://reactjs.org) - JavaScript Library
- [TailwindCSS](https://tailwindcss.com) - CSS Framework
- [DaisyUI](https://daisyui.com) - Component Library
- [Vite](https://vitejs.dev) - Build Tool
