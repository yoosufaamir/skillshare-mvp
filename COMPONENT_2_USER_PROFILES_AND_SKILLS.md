# Component 2: User Profiles & Skills Management

## Team Member Assignment
**Assigned to: [Team Member 2 Name]**

## What This Component Includes

### Backend Files:
- `backend/src/controllers/userController.js`
- `backend/src/routes/users.js`
- `backend/src/models/User.js` (profile-related schemas)
- `backend/src/middleware/validation.js`

### Frontend Files:
- `frontend/src/pages/ProfilePage.jsx`
- `frontend/src/pages/SettingsPage.jsx`
- `frontend/src/components/ui/Input.jsx`
- `frontend/src/components/ui/Button.jsx`
- `frontend/src/components/ui/Card.jsx`
- `frontend/src/services/api.js` (user-related endpoints)

## Key Features to Implement:
1. User profile creation and editing
2. Skills management (offered and desired skills)
3. Profile picture upload
4. Bio and location management
5. User statistics tracking
6. Profile validation and sanitization
7. User preferences and settings

## API Endpoints to Implement:
- `GET /api/users/:userId`
- `PUT /api/users/profile`
- `POST /api/users/skill-verification`
- `GET /api/users/profile`
- `PUT /api/users/settings`

## Dependencies to Install:
```bash
# Backend
npm install multer cloudinary express-validator

# Frontend
npm install react-dropzone react-image-crop
```

## Testing Checklist:
- [ ] User can create a complete profile
- [ ] Skills can be added, edited, and removed
- [ ] Profile picture upload works
- [ ] Profile validation prevents invalid data
- [ ] User statistics are calculated correctly
- [ ] Settings are saved and retrieved properly

## Integration Points:
- Depends on Component 1 (Authentication)
- Provides user data for Component 3 (Matching)
- User profiles are displayed in Component 4 (Chat)
- Profile data is used in Component 5 (Sessions)

## Files to Create/Modify:
1. Create comprehensive user profile forms
2. Implement file upload for profile pictures
3. Add skill management interface
4. Create user settings page
5. Implement profile validation

## Key Components to Build:
1. **ProfileForm Component**: Complete profile editing form
2. **SkillsManager Component**: Add/edit/remove skills
3. **ProfilePictureUpload Component**: Image upload with preview
4. **UserStats Component**: Display user statistics
5. **SettingsPanel Component**: User preferences

## Notes:
- Focus on user experience and intuitive interface
- Implement proper form validation
- Ensure responsive design for mobile devices
- Add loading states and error handling
- Consider accessibility features
