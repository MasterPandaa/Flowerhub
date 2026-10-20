# Flowerhub — Florist & Flower Order E-Commerce Platform

A modern flower boutique and order management e-commerce web application built with **Laravel 11**, designed for florists and gifting businesses.

Flowerhub streamlines customer bouquet browsing, order scheduling, and checkout while providing shop administrators with an end-to-end order processing and inventory dashboard.

---

## Features

- **Product Showcase**: Catalog for flower bouquets, standing flower arrangements, and gift hampers with multi-image support.
- **Order Scheduling & Customization**: Support for delivery date selection, greeting card message customization, and recipient details.
- **Payment Gateway Integration**: Secure checkout supporting online payments, bank transfers, and e-wallets via Midtrans Snap.
- **Order Management Dashboard**: Real-time status tracking for store admins (Pending, In Arrangement, Out for Delivery, Completed).
- **Role & Permission Management**: Multi-tier access control (Store Admin, Florist Staff, Customer) powered by Spatie Permission.
- **Image Processing**: Automatic thumbnail optimization and aspect-ratio handling for flower photographs via Intervention Image.

---

## Tech Stack

- **Backend**: Laravel 11, PHP 8.2+
- **Frontend**: Blade Templates, Tailwind CSS / Bootstrap, JavaScript
- **Database**: MySQL / SQLite
- **Payment Gateway**: Midtrans Snap Integration
- **Key Packages**:
  - `spatie/laravel-permission` (Role-based access control)
  - `intervention/image` (Media optimization)
  - `laravel/sanctum` & `laravel/socialite` (Authentication)

---

## Getting Started

### Prerequisites

- PHP >= 8.2
- Composer
- Node.js & NPM
- MySQL or SQLite
- Midtrans Merchant Sandbox Account (for payment testing)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/MasterPandaa/Flowerhub.git
   cd Flowerhub
   ```

2. **Install PHP and JavaScript dependencies**:
   ```bash
   composer install
   npm install && npm run build
   ```

3. **Configure environment**:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Update payment & database credentials in `.env`**:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=flowerhub_db
   DB_USERNAME=root
   DB_PASSWORD=

   MIDTRANS_SERVER_KEY=your_sandbox_server_key
   MIDTRANS_CLIENT_KEY=your_sandbox_client_key
   MIDTRANS_IS_PRODUCTION=false
   ```

5. **Run migrations and seeders**:
   ```bash
   php artisan migrate --seed
   php artisan storage:link
   ```

6. **Start the application**:
   ```bash
   php artisan serve
   ```
   Access the store at `http://127.0.0.1:8000`.

---

## License

This project is licensed under the [MIT License](LICENSE).
