# 📁 Multiple Data Files Guide

## Overview

Your Multi QR Manager now supports multiple JSON data files for organizing users by location, department, or any other category you prefer.

## 🗂️ Current Data Files

- `data/clients.json` - Main users file
- `data/personal.json` - Personal user accounts
- Add more files as needed!

## ➕ Adding New Data Files

### Method 1: Manual Setup

1. **Create a new JSON file** in the `data/` folder:
   ```
   data/users_location2.json
   data/users_office.json
   data/users_store.json
   ```

2. **Update the data file lists** in these files:
   - `script.js` (line 24-28)
   - `user.html` (line 194-198) 
   - `edit.html` (line 351-355)

3. **Add your file path** to each list:
   ```javascript
   const dataFiles = [
     './data/clients.json',
     './data/personal.json',
     './data/users_location2.json',  // Add your new file here
     './data/users_office.json'       // And here
   ];
   ```

### Method 2: Using Data Manager (Advanced)

1. **Data files are automatically managed** by the main application:
   - The system automatically loads from `data/personal.json` and `data/clients.json`
   - Additional data files can be added to the `dataFiles` array in `script.js`

2. **Current data file structure**:
   ```javascript
   // In script.js, the dataFiles array is defined as:
   const dataFiles = [
     './data/personal.json',
     './data/clients.json',
     // Add more files here as needed
   ];
   ```

## 📋 Data File Structure

Each data file should follow this structure:

```json
[
  {
    "username": "user1",
    "fullname": "User One",
    "userCode": "U12024ABC",
    "email": "user1@example.com",
    "phone": "+1234567890",
    "website": "https://user1.com",
    "location": "https://maps.app.goo.gl/...",
    "linkedin": "https://linkedin.com/in/user1",
    // ... all other platform fields
  }
]
```

## 🔧 Configuration Locations

Update these files when adding new data files:

### 1. Dashboard (script.js)
```javascript
// Line 24-28
const dataFiles = [
  './data/clients.json',
  './data/personal.json',
  './data/users_newlocation.json'  // Add here
];
```

### 2. User Profile (user.html)
```javascript
// Line 194-198
const dataFiles = [
  './data/clients.json',
  './data/personal.json',
  './data/users_newlocation.json'  // Add here
];
```

### 3. Edit Form (edit.html)
```javascript
// Line 351-355
const dataFiles = [
  './data/clients.json',
  './data/personal.json',
  './data/users_newlocation.json'  // Add here
];
```

## 🎯 Benefits

- **Organize by location**: Different files for different locations
- **Department separation**: Separate files for different departments
- **Easy management**: Add/remove locations without affecting others
- **Scalability**: Handle unlimited users across multiple files
- **Backup friendly**: Easy to backup individual location data

## 📝 Example Use Cases

### Location-Based Organization
```
data/clients.json              # Main office
data/personal.json           # Personal accounts
data/users_downtown.json     # Downtown location
data/users_airport.json      # Airport kiosk
```

### Department-Based Organization
```
data/clients.json              # General users
data/users_sales.json        # Sales team
data/users_support.json      # Support team
data/users_management.json   # Management
```

### Event-Based Organization
```
data/clients.json              # Regular users
data/users_conference.json   # Conference attendees
data/users_trade_show.json   # Trade show participants
```

## 🚀 Quick Start

1. **Create your new data file**:
   ```bash
   # Copy existing file as template
   cp data/clients.json data/users_newlocation.json
   ```

2. **Update the three configuration locations** mentioned above

3. **Add your users** to the new file using the edit form

4. **Test** by creating a QR code and scanning it

## 🔍 Troubleshooting

### Users Not Showing Up
- Check that the file path is added to all three configuration locations
- Verify the JSON file is valid (use a JSON validator)
- Check browser console for error messages

### Duplicate User Codes
- The system automatically checks across all files for unique codes
- If you get duplicate errors, the user code generation will handle it

### File Not Found Errors
- Ensure the file exists in the `data/` folder
- Check the file path spelling in all three locations
- Verify file permissions

## 📊 Monitoring

Check the browser console for loading messages:
```
✅ Loaded 5 users from ./data/clients.json
✅ Loaded 3 users from ./data/personal.json
📊 Total users loaded: 8
```

## 🎉 That's It!

Your Multi QR Manager now supports unlimited data files for perfect organization by location, department, or any other category you need!
