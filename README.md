# Setup Guide for Different Laptops

This guide will help you run the Bharat Panchayat Transparency app on any Windows laptop.

## Prerequisites

Before running `StartApp.bat`, ensure the following software is installed:

### 1. **Python 3.8 or Higher**
- Download from: https://www.python.org/downloads/
- **IMPORTANT**: During installation, check "Add Python to PATH"
- Verify installation:
  ```bash
  python --version
  ```

### 2. **Node.js (includes npm)**
- Download from: https://nodejs.org/ (LTS version recommended)
- **IMPORTANT**: This automatically installs npm
- Verify installation:
  ```bash
  node --version
  npm --version
  ```

## Quick Start

### Option 1: Automatic Setup (Recommended)
1. Double-click `StartApp.bat`
2. The script will automatically:
   - Check if Python and Node.js are installed
   - Create virtual environment if needed
   - Install all dependencies
   - Start both backend and frontend servers
   - Open the app in your browser

### Option 2: Manual Setup

#### Backend Setup
```bash
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

#### Frontend Setup (in a new terminal)
```bash
cd frontend
npm install
npm start
```

## Common Issues and Solutions

### Issue 1: "Python is not recognized"
**Solution**: Python is not installed or not in PATH
- Reinstall Python and check "Add Python to PATH"
- Or manually add Python to system PATH

### Issue 2: "Node is not recognized"
**Solution**: Node.js is not installed or not in PATH
- Install Node.js from https://nodejs.org/
- Restart your terminal/command prompt

### Issue 3: "Port already in use"
**Solution**: Another application is using port 8000 or 3000
- Close other applications using these ports
- Or modify the ports in:
  - Backend: `StartApp.bat` line with `--port 8000`
  - Frontend: Create `.env` file with `PORT=3001`

### Issue 4: "Module not found" errors
**Solution**: Dependencies not installed
- Backend: Run `pip install -r requirements.txt` in backend folder
- Frontend: Run `npm install` in frontend folder

### Issue 5: Virtual environment activation fails
**Solution**: 
- Delete the `backend\venv` folder
- Run `StartApp.bat` again to recreate it

### Issue 6: Frontend doesn't start
**Solution**:
- Delete `frontend\node_modules` folder
- Delete `frontend\package-lock.json`
- Run `npm install` again in frontend folder

## File Structure
```
BHARAT PANCHAYAT TRANSPARENCY/
├── backend/
│   ├── venv/              (auto-created)
│   ├── main.py
│   ├── requirements.txt
│   └── ...
├── frontend/
│   ├── node_modules/      (auto-created)
│   ├── package.json
│   ├── src/
│   └── ...
├── StartApp.bat           (run this!)
└── SETUP_GUIDE.md         (this file)
```

## First-Time Setup Checklist

- [ ] Install Python 3.8+ (with PATH option checked)
- [ ] Install Node.js LTS (includes npm)
- [ ] Download/Copy the entire project folder
- [ ] Run `StartApp.bat`
- [ ] Wait for automatic setup to complete
- [ ] Browser should open automatically to http://localhost:3000

## Access Points

After successful startup:
- **Frontend (UI)**: http://localhost:3000
- **Backend (API)**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs
- **API Alternative Docs**: http://localhost:8000/redoc

## Stopping the Application

1. Close the browser
2. In each terminal window (Backend Server & Frontend Server):
   - Press `Ctrl + C`
   - Type `Y` when asked to terminate
3. Or simply close both terminal windows

## Transferring to Another Laptop

### What to Copy:
- ✅ Entire project folder
- ✅ All source code files

### What NOT to Copy (will be auto-created):
- ❌ `backend\venv\` folder
- ❌ `frontend\node_modules\` folder
- ❌ `backend\__pycache__\` folders
- ❌ `.pyc` files

### Recommended: Create a ZIP without dependencies
```bash
# Exclude these folders when creating ZIP:
- backend/venv/
- frontend/node_modules/
- **/__pycache__/
- **/*.pyc
```

## Need Help?

If you encounter issues:
1. Check the error message in the terminal
2. Refer to "Common Issues" section above
3. Ensure Python and Node.js are properly installed
4. Try manual setup (Option 2) to see detailed error messages

## System Requirements












# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
