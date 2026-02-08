# Component 1: Authentication & User Management

## Team Member Assignment
**Assigned to: [Team Member 1 Name]**

## What This Component Includes

### Backend Files:
- `backend/src/working-server.js` (Authentication routes only)
- `backend/src/controllers/authController.js`
- `backend/src/middleware/auth.js`
- `backend/src/models/User.js`
- `backend/src/routes/auth.js`

### Frontend Files:
- `frontend/src/pages/auth/LoginPage.jsx`
- `frontend/src/pages/auth/RegisterPage.jsx`
- `frontend/src/pages/auth/SimpleLoginPage.jsx`
- `frontend/src/components/auth/ProtectedRoute.jsx`
- `frontend/src/components/auth/AdminRoute.jsx`
- `frontend/src/stores/auth.js`
- `frontend/src/stores/authStore.js`
- `frontend/src/services/authService.js`

## Key Features to Implement:
1. User registration with validation
2. User login with JWT tokens
3. Password hashing with bcrypt
4. Protected routes middleware
5. Admin role management
6. User session management
7. Authentication state management (Zustand)

## API Endpoints to Implement:
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/me`
- `PUT /api/users/profile` (basic profile updates)

## Dependencies to Install:
```bash
# Backend
npm install bcryptjs jsonwebtoken express-validator

# Frontend
npm install zustand axios
```

## Testing Checklist:
- [ ] User can register with valid data
- [ ] User can login with correct credentials
- [ ] Protected routes redirect unauthenticated users
- [ ] JWT tokens are properly generated and validated
- [ ] Admin routes are protected
- [ ] User session persists on page refresh

## Integration Points:
- This component provides the foundation for all other components
- Other components will depend on the authentication system
- User data structure must be consistent across all components

## Files to Create/Modify:
1. Extract authentication routes from `working-server.js`
2. Create separate auth controller
3. Implement proper error handling
4. Add input validation
5. Create comprehensive auth store

## Notes:
- This is the most critical component as others depend on it
- Focus on security best practices
- Ensure proper error messages for user feedback
- Test with both valid and invalid inputs
