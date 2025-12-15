# 🔐 Admin Credentials Management

## Overview
Admin credentials are stored in `credentials/login_credentials.json` and can be easily managed by editing this file.

## File Structure
```json
[
  {
    "username": "admin",
    "password": "@Class3718",
    "role": "admin",
    "createdAt": "2024-01-01",
    "isActive": true
  }
]
```

## Adding New Admin Users

### Method 1: Direct JSON Editing
1. Open `credentials/login_credentials.json`
2. Add a new admin object to the array:

```json
[
  {
    "username": "admin",
    "password": "@Class3718",
    "role": "admin",
    "createdAt": "2024-01-01",
    "isActive": true
  },
  {
    "username": "manager",
    "password": "ManagerPass123",
    "role": "admin",
    "createdAt": "2024-01-15",
    "isActive": true
  }
]
```

### Method 2: Using the Edit Form
1. Go to `edit.html`
2. Fill in the admin credentials form
3. Copy the generated JSON
4. Add it to `credentials/login_credentials.json`

## Field Descriptions

- **username**: The login username (required)
- **password**: The login password (required)
- **role**: User role (currently only "admin" supported)
- **createdAt**: Date when the account was created (optional)
- **isActive**: Whether the account is active (true/false)

## Security Notes

⚠️ **Important Security Considerations:**

1. **File Protection**: Ensure `credentials/login_credentials.json` is not publicly accessible
2. **Strong Passwords**: Use strong, unique passwords for each admin
3. **Regular Updates**: Change passwords periodically
4. **Backup**: Keep a secure backup of credentials
5. **Access Control**: Limit who can edit the credentials file

## Deactivating Users

To temporarily disable an admin without deleting them:
```json
{
  "username": "oldadmin",
  "password": "OldPass123",
  "role": "admin",
  "createdAt": "2024-01-01",
  "isActive": false
}
```

## Removing Users

Simply delete the entire user object from the JSON array.

## Default Credentials

- **Username**: `admin`
- **Password**: `@Class3718`

**⚠️ Change these default credentials immediately after setup!**
