# AEGIS Reports System - Login Information

## 🔐 Access Information

**Login URL**: `login.html`

### Default Credentials

```
Username: admin
Password: aegis337
```

## 🌐 Pages

1. **login.html** - Login page (entry point)
2. **index.html** - AEGIS system introduction page
3. **AEGIS/Aegis_Dashboard.html** - Reports dashboard

## 🔒 Security Features

- **Session-based authentication** using `sessionStorage`
- **Password hashing** with SHA-256
- **Session timeout**: 4 hours
- **Automatic redirect** to login page if not authenticated
- **Logout button** on all protected pages
- **Keyboard shortcut**: `Ctrl+L` (or `Cmd+L` on Mac) to logout

## 🛠️ Changing Password

To change the password, you need to:

1. Generate a new SHA-256 hash of your password:

```bash
# Using Python
python3 -c "import hashlib; print(hashlib.sha256('YOUR_NEW_PASSWORD'.encode()).hexdigest())"

# Using Node.js
node -e "console.log(require('crypto').createHash('sha256').update('YOUR_NEW_PASSWORD').digest('hex'))"

# Using online tool
# Visit: https://emn178.github.io/online-tools/sha256.html
```

2. Replace the hash in `login.html` (line ~35):

```javascript
const VALID_PASSWORD_HASH = 'YOUR_NEW_HASH_HERE';
```

## 📝 Notes

- This is a **client-side authentication** system
- For production use, implement **server-side authentication**
- Store credentials securely (not hardcoded)
- Consider using environment variables or a backend API
- Add HTTPS for secure transmission

## 🚀 Deployment

When deploying to a production server:

1. Use HTTPS (SSL/TLS)
2. Implement server-side authentication
3. Use proper session management (JWT, cookies)
4. Add rate limiting to prevent brute-force attacks
5. Implement proper password policies
6. Add 2FA (Two-Factor Authentication) if needed

---

**AEGIS System v4.0** | "Investing at the Speed of AI"
