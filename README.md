![image](https://github.com/RadhaPriyadarshan/password-reset-api/assets/70469801/6a111990-9836-49cd-8480-444d2e23ca97)

# Password Reset Application

This repository contains two parts of the Password Reset Application:

1. **Frontend**: A React application hosted on Netlify.
   **Hosted URL**: [Click here](https://password-reset-site.netlify.app)
2. **Backend**: An Express.js API hosted on Render.
   **Hosted URL**: [Click here](https://password-reset-api-7lem.onrender.com) 

## Table of Contents

- [Frontend Setup](#frontend-setup)
- [Backend Setup](#backend-setup)
- [Deployment](#deployment)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Frontend Setup

### Prerequisites

- Node.js and npm installed on your local machine.

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/password-reset-frontend.git
   cd password-reset-frontend
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:

   ```env
   REACT_APP_API_URL=https://password-reset-api-7lem.onrender.com
   ```

### Running Locally

```sh
npm start
```

The application will run on `http://localhost:3000`.

### File Structure

- `src/`: Contains all the source code.
  - `components/`: Contains React components.
  - `App.js`: Main application component.
  - `index.js`: Entry point for the React application.

### Deployment

The frontend is deployed on Netlify. To deploy:

1. Push your changes to GitHub.
2. Go to [Netlify](https://www.netlify.com/).
3. Connect your GitHub repository.
4. Configure build settings:
   - Build Command: `npm run build`
   - Publish Directory: `build`

**Hosted URL**: [Password Reset Frontend](https://password-reset-site.netlify.app)

## Backend Setup

### Prerequisites

- Node.js and npm installed on your local machine.
- MongoDB Atlas account.

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/password-reset-backend.git
   cd password-reset-backend
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:

   ```env
   MONGO_URI=mongodb+srv://yourMongoDBURI
   HOST=Gmail
   GMAIL_USER=yourGMAILUser
   GMAIL_PASS=yourGMAILPass
   CLIENT_URL=https://password-reset-site.netlify.app
   ```

### Running Locally

```sh
npm start
```

The application will run on `http://localhost:5000`.

### File Structure

- `models/`: Contains Mongoose models.
  - `User.js`: User model schema.
- `routes/`: Contains route definitions.
- `index.js`: Entry point for the Express application.

### Deployment

The backend is deployed on Render. To deploy:

1. Push your changes to GitHub.
2. Go to [Render](https://render.com/).
3. Create a new Web Service.
4. Connect your GitHub repository.
5. Configure environment variables based on your `.env` file.

**Hosted URL**: [Password Reset API](https://password-reset-api-7lem.onrender.com)

## Usage

### Password Reset Workflow

1. **Request Password Reset**:
   - User submits their email on the [Forgot Password Page](https://password-reset-site.netlify.app/forgot-password).
   - The backend generates a reset token and sends an email with a reset link.

2. **Reset Password**:
   - User clicks the link in the email, leading to the [Reset Password Page](https://password-reset-site.netlify.app/reset-password/:token).
   - User submits their new password.
   - The backend verifies the token, updates the password, and removes the reset token.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

