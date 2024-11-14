# KotlinBois - Gagambrawl Backend API

## Project Description

**Gagambrawl** is an easy-to-use app for spider lovers and breeders. It helps you keep track of your spiders, including how many you have, their health, and breeding details.

## Team Members

**ELDROID Team:**
- [Andrino](https://github.com/andrino25) - Alliance
- [Apiag](https://github.com/Kevinboo123)
- [Diamos](https://github.com/diamosclint)
- [Fuentes](https://github.com/nostraJello)
- [Villariasa](https://github.com/vjoseph6)

**ELPHP Team:**
- [Sufficiencia]()

## Repository Links
- **Android Repository**: [ELDROID_KotlinBois_-130FRI-](https://github.com/andrino25/ELDROID_KotlinBois_-130FRI-)
- **PHP Repository**: [ELPHP_KotlinBois_-130SAT-](https://github.com/vjoseph6/ELPHP_KotlinBois_-130SAT-)

## Documentation
- [Project Documentation](https://docs.google.com/document/d/1bLO-Mcyeix4iPgywo0olDADMsDcrTcbylMeiVZxSI7A/edit?tab=t.0)

-----------------------------------------------------------------------------------------------------------------------

## Technical Setup

### Prerequisites
- PHP >= 8.1
- Composer
- SQLite (for development)

### Local Development Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/vjoseph6/ELPHP_KotlinBois_-130SAT-
   cd ELPHP_KotlinBois_-130SAT-
   ```

2. **Install Dependencies**
   ```bash
   composer install
   ```

3. **Environment Configuration**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Database Setup**
   ```bash
   # Create SQLite database
   touch database/database.sqlite
   
   # Run migrations
   php artisan migrate
   ```

5. **Start Local Development Server**
   ```bash
   php artisan serve
   ```
   The API will be available at `http://localhost:8000`

## API Documentation

### Authentication Endpoints

#### Register User

http
POST /api/auth/register
Request Body:
{
"email": "user@example.com",
"password": "password123",
"password_confirmation": "password123"
}
Response (201 Success):
{
"success": true,
"message": "Registration successful",
"token": "your-auth-token",
"user": {
"id": 1,
"email": "user@example.com",
"name": "user"
}
}

#### Login User

http
POST /api/auth/login
Request Body:
{
"email": "user@example.com",
"password": "password123"
}
Response (200 Success):
{
"success": true,
"message": "Login successful",
"token": "your-auth-token",
"user": {
"id": 1,
"email": "user@example.com",
"name": "user"
}
}

## Error Responses

json
{
"success": false,
"message": "Error message here"
}


Common HTTP Status Codes:
- 422: Validation Error
- 401: Unauthorized
- 500: Server Error

## Development Workflow

1. Create a new branch for your feature
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and commit
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```

3. Push to GitHub
   ```bash
   git push origin feature/your-feature-name
   ```

4. Create a Pull Request to the `develop` branch

## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Security
If you discover any security-related issues, please email the team instead of using the issue tracker.