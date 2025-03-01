# Hospital GUI Project Setup Guide

## Prerequisites
- Node.js installed
- MongoDB account created
- Git installed
- Code editor (VS Code recommended)

## Step by Step Setup

1. Clone the repository:
```bash
git clone [your-repository-url]
cd SD1_Final
```

2. Install Dependencies:
```bash
# Install root dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..

# Install backend dependencies
cd backend
npm install
cd ..
```

3. Database Setup:
Create a .env file in the backend directory with:
```
MONGODB_URI=mongodb+srv://[username]:[password]@cluster0.ygv7r.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
```
Replace [username] and [password] with provided MongoDB credentials

## Project Structure
```
Hospital_GUI/
├── frontend/
│   ├── public/
│   └── src/
│       ├── pages/
│       │   ├── MainDashboard.js
│       │   ├── Entertainment.js
│       │   ├── PatientInfo.js
│       │   ├── CallNurse.js
│       │   └── Settings.js
│       ├── styles/
│       │   └── TVMode.css
│       └── context/
├── backend/
│   ├── models/
│   ├── server.js
│   └── .env
└── main.js
```

## Running the Project

1. Start backend server:
```bash
cd backend
node server.js
```

2. In a new terminal, start frontend:
```bash
cd frontend
npm start
```

3. In another terminal, start Electron (from root directory):
```bash
npm run dev
```

## Available Scripts
```bash
# Development mode (runs everything)
npm run dev

# Start frontend only
npm run react-start

# Start electron only
npm start
```

## Current Features
- Real-time clock display
- Patient information display
- Patient switching functionality
- Basic navigation
- Database integration

## Working on the Project

1. Always pull latest changes before starting:
```bash
git pull origin main
```

2. Create new branch for features:
```bash
git checkout -b feature/your-feature-name
```

3. Make changes and commit:
```bash
git add .
git commit -m "Description of changes"
git push origin feature/your-feature-name
```

4. Create pull request on GitHub

## Testing Database Connection
```bash
# In backend directory
cd backend
node testDb.js
```

## Important Notes
- Never commit .env files
- Always pull latest changes before starting work
- Create new branches for features
- Follow the existing style guide
- Test features locally before pushing

## Current Technologies Used
- Frontend: React.js
- Backend: Node.js, Express.js
- Database: MongoDB
- Desktop: Electron
- State Management: React Hooks
- Routing: React Router

## Troubleshooting Common Issues
1. If modules are missing:
```bash
npm install
```

2. If database connection fails:
- Check .env file exists
- Verify MongoDB credentials
- Ensure MongoDB service is running

3. If frontend won't start:
- Check if port 3000 is available
- Verify all dependencies are installed

4. If Electron won't start:
- Make sure frontend is running first
- Check main.js configuration

## Getting Help
If you encounter any issues:
1. Check the error logs
2. Consult the project documentation
3. Ask team members for help
4. Check GitHub issues

Remember to keep your repository up to date and communicate with team members about the features you're working on!
