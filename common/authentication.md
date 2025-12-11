# Authentication

**Navigation**: [Home](../README.md) > [Common Documentation](../README.md#common-topics) > Authentication

## Overview

The Vendor Portal uses secure JWT (JSON Web Token) based authentication to protect user accounts and ensure only authorized users can access the system. This page explains how to sign in, manage your password, and understand session handling.

## Key Concepts

### JWT Tokens

When you sign in successfully, the system generates a secure JWT token that:
- Identifies you as an authenticated user
- Contains your user ID and role information
- Expires after a set period for security
- Must be included with every request to protected resources

### User Roles

The system supports different user roles with varying access levels:
- **Admin**: Full system access including user management, batch approval, and system configuration
- **Vendor User**: Access to product submission, batch tracking, and vendor-specific features
- **Internal Reviewer**: Similar to admin with review capabilities

### Account Status

Your account can have different statuses:
- **Active**: Full access to the system
- **Pending Approval**: Account created but awaiting admin approval (cannot sign in)
- **Inactive**: Account deactivated by admin (cannot sign in)

## Sign-In Process

### Accessing the Sign-In Page

1. Navigate to the Vendor Portal URL
2. You'll be automatically redirected to the sign-in page if not authenticated
3. The sign-in page displays the ChopAir Vendor Portal branding and login form

### Signing In

**Step 1: Enter Your Email**
- Enter your registered email address in the "Email Address" field
- The system validates email format in real-time
- Invalid email formats will show an error message

**Step 2: Enter Your Password**
- Enter your password in the "Password" field
- Click the eye icon to toggle password visibility if needed
- Passwords are masked by default for security

**Step 3: Submit**
- Click the "Sign In" button to authenticate
- The button will show "Signing in..." while processing
- You'll be redirected to your dashboard upon successful authentication

### Sign-In Validation

The system performs several checks during sign-in:

1. **Email Format**: Must be a valid email address format
2. **Credentials**: Email and password must match an existing account
3. **Account Status**: Account must be active and approved
4. **Password Verification**: Uses PBKDF2-HMAC-SHA256 hashing for secure password verification

### Successful Sign-In

When you sign in successfully:
- A success message appears: "Welcome back! Logged in as [your email]"
- You're redirected based on your role:
  - **Admin users**: Redirected to `/admin/dashboard`
  - **Vendor users**: Redirected to `/vendor/dashboard`
- A JWT token is stored securely in your browser
- Your session begins and remains active until expiration or logout

### Sign-In Errors

The system provides clear error messages for different scenarios:

**Invalid Credentials**
- **Message**: "Invalid Credentials - The email or password you entered is incorrect"
- **Cause**: Email or password doesn't match any account
- **Solution**: Double-check your email and password, or use "Forgot password?" link

**Account Pending Approval**
- **Message**: "Account Pending Approval - Your account is awaiting admin approval. Please check back later."
- **Cause**: Your account has been created but not yet approved by an administrator
- **Solution**: Wait for admin approval or contact support

**Account Inactive**
- **Message**: "Account Inactive - Your account has been deactivated. Please contact support."
- **Cause**: Your account has been deactivated by an administrator
- **Solution**: Contact support to inquire about reactivation

**General Login Failure**
- **Message**: "Login Failed - [error details]"
- **Cause**: System error or network issue
- **Solution**: Try again or contact support if the issue persists

## Password Management

### Password Requirements

When creating or changing your password, ensure it meets these requirements:
- Minimum length (typically 8 characters)
- Combination of letters, numbers, and special characters recommended
- Should not be easily guessable or commonly used

### Password Security

The Vendor Portal uses industry-standard security practices:
- **Hashing Algorithm**: PBKDF2-HMAC-SHA256 with 200,000 iterations
- **Salt**: Unique 16-byte random salt for each password
- **Storage Format**: `pbkdf2$iterations$salt$hash`
- **Verification**: Constant-time comparison to prevent timing attacks

Your password is never stored in plain text and cannot be retrieved by administrators.

### Forgot Password

If you forget your password:

1. Click the "Forgot password?" link on the sign-in page
2. Enter your registered email address
3. Follow the instructions sent to your email
4. Create a new password that meets the requirements
5. Sign in with your new password

**Note**: Password reset links expire after a set period for security.

### Changing Your Password

To change your password while signed in:

1. Navigate to your profile settings
2. Click on "Settings" in the navigation menu
3. Find the "Password" section
4. Enter your current password
5. Enter your new password
6. Confirm your new password
7. Click "Save" to update

You'll be required to sign in again with your new password.

## Session Management

### Session Duration

Your session remains active for a set period (typically 60 minutes) after sign-in. The JWT token contains an expiration timestamp that the system checks with every request.

### Token Expiration

When your token expires:
- You'll be automatically redirected to the sign-in page
- Any unsaved work may be lost
- You'll need to sign in again to continue

**Best Practice**: Save your work frequently to avoid data loss.

### Session Validation

The system validates your session on every request:
1. Checks if a valid JWT token is present
2. Verifies the token signature
3. Checks if the token has expired
4. Validates that the user still exists and is active
5. Verifies user permissions for the requested resource

### Automatic Logout

You'll be automatically logged out if:
- Your JWT token expires
- Your account is deactivated by an administrator
- Your account is deleted
- The token signature is invalid or tampered with

### Manual Logout

To sign out manually:

1. Click on your profile icon or name in the header
2. Select "Logout" from the dropdown menu
3. You'll be redirected to the sign-in page
4. Your JWT token will be removed from the browser

**Security Tip**: Always log out when using shared or public computers.

## Security Best Practices

### Protecting Your Account

1. **Use a Strong Password**
   - Minimum 8 characters
   - Mix of uppercase, lowercase, numbers, and symbols
   - Avoid common words or personal information
   - Don't reuse passwords from other sites

2. **Keep Your Credentials Private**
   - Never share your password with anyone
   - Don't write down your password
   - Be cautious of phishing attempts

3. **Sign Out When Done**
   - Always log out on shared computers
   - Close your browser after logging out on public devices
   - Don't leave your session unattended

4. **Monitor Your Account**
   - Review your account activity regularly
   - Report any suspicious activity immediately
   - Update your password if you suspect compromise

### Browser Security

For optimal security:
- Use a modern, updated web browser
- Enable browser security features
- Clear browser cache and cookies periodically
- Avoid browser extensions that may intercept data

### Network Security

When accessing the Vendor Portal:
- Use secure, trusted networks when possible
- Avoid public Wi-Fi for sensitive operations
- Consider using a VPN on untrusted networks
- Ensure the URL shows HTTPS (secure connection)

## Troubleshooting

### Cannot Sign In

**Problem**: Sign-in button is disabled
- **Cause**: Email format is invalid or fields are empty
- **Solution**: Ensure email is properly formatted and all fields are filled

**Problem**: "Invalid token" error after sign-in
- **Cause**: Token generation or storage issue
- **Solution**: Clear browser cache and cookies, try again

**Problem**: Redirected back to sign-in page immediately
- **Cause**: Token not being stored properly
- **Solution**: Check browser settings allow cookies, disable strict privacy modes temporarily

### Session Issues

**Problem**: Frequently logged out
- **Cause**: Short token expiration or browser not storing token
- **Solution**: Check browser cookie settings, contact support if issue persists

**Problem**: "Token expired" error
- **Cause**: Your session has timed out
- **Solution**: Sign in again to get a new token

**Problem**: Access denied after sign-in
- **Cause**: Account status changed or permissions revoked
- **Solution**: Contact your administrator

### Password Issues

**Problem**: Forgot password link not working
- **Cause**: Email not registered or system issue
- **Solution**: Verify email address, contact support

**Problem**: Cannot reset password
- **Cause**: Reset link expired or already used
- **Solution**: Request a new password reset link

**Problem**: New password rejected
- **Cause**: Doesn't meet password requirements
- **Solution**: Ensure password meets all requirements

## Related Topics

### User Settings
- **Admin Settings** - Managing your admin profile and password
- **[Vendor Settings](../vendor/settings.md)** - Managing your vendor profile and password

### Getting Started
- **Admin Getting Started** - First-time login for admins
- **[Vendor Getting Started](../vendor/getting-started.md)** - First-time login for vendors

### Common Documentation
- **[Notifications System](./notifications-system.md)** - Understanding notifications
- **[Troubleshooting](./troubleshooting.md)** - Solutions for authentication issues

---

**Back to**: [Home](../README.md)

## Support

If you encounter authentication issues that you cannot resolve:
- Contact your system administrator
- Email support with details of the issue
- Include any error messages you received
- Specify your browser and operating system

**Security Note**: Never share your password or JWT token with support staff. They will never ask for this information.
