# Troubleshooting and FAQ

**Navigation**: [Home](../README.md) > [Common Documentation](../README.md#common-topics) > Troubleshooting

## Overview

This guide provides solutions to common issues you may encounter while using the Vendor Portal. Whether you're experiencing login problems, upload errors, or other technical difficulties, this page will help you resolve issues quickly and get back to work.

If you can't find a solution to your problem here, please contact support using the information at the bottom of this page.

## Common Issues and Solutions

### Authentication and Login Issues

#### Cannot Sign In - Invalid Credentials

**Problem**: You receive an "Invalid Credentials" error when trying to sign in.

**Possible Causes**:
- Incorrect email address or password
- Account doesn't exist in the system
- Typing error or caps lock enabled

**Solutions**:
1. Double-check your email address for typos
2. Verify your password is correct (check caps lock)
3. Try copying and pasting your credentials to avoid typing errors
4. Use the "Forgot password?" link to reset your password
5. Contact your administrator to verify your account exists

#### Account Pending Approval

**Problem**: You receive an "Account Pending Approval" message when trying to sign in.

**Cause**: Your account has been created but not yet approved by an administrator.

**Solutions**:
1. Wait for an administrator to approve your account
2. Check your email for approval notifications
3. Contact your administrator to request approval
4. Typical approval time: 1-2 business days

#### Account Inactive

**Problem**: You receive an "Account Inactive" message when trying to sign in.

**Cause**: Your account has been deactivated by an administrator.

**Solutions**:
1. Contact your administrator to inquire about reactivation
2. Verify you're using the correct email address
3. Ask about the reason for deactivation
4. Request account reactivation if appropriate

#### Session Expired / Automatically Logged Out

**Problem**: You're frequently logged out or see "Session expired" messages.

**Possible Causes**:
- JWT token has expired (typically after 60 minutes of inactivity)
- Browser not storing authentication token properly
- Multiple tabs or windows causing conflicts

**Solutions**:
1. Sign in again to get a new session token
2. Save your work frequently to avoid data loss
3. Check browser settings allow cookies and local storage
4. Disable strict privacy modes that block cookies
5. Close other tabs/windows with the Vendor Portal open
6. Clear browser cache and cookies, then sign in again

#### Cannot Access Certain Pages

**Problem**: You get "Access Denied" or are redirected when trying to access certain pages.

**Possible Causes**:
- Insufficient permissions for your role
- Session expired
- Account status changed

**Solutions**:
1. Verify you're signed in (check for your name in the header)
2. Confirm your user role has access to that feature
3. Sign out and sign in again to refresh permissions
4. Contact your administrator if you need additional permissions

### File Upload Issues

#### File Upload Fails Immediately

**Problem**: File upload fails as soon as you select the file.

**Possible Causes**:
- File size exceeds 10MB limit
- File format is not supported (.xlsx or .xls required)
- File is corrupted or unreadable
- Network connectivity issues

**Solutions**:
1. Check file size - must be under 10MB
   - Right-click file → Properties to see size
   - Compress file by removing unnecessary formatting or splitting into smaller batches
2. Verify file format is .xlsx or .xls
   - Save as Excel Workbook (.xlsx) if using different format
3. Try opening the file in Excel to verify it's not corrupted
4. Check your internet connection
5. Try a different browser
6. Clear browser cache and cookies

#### File Parsing Takes Too Long

**Problem**: The "Preview Upload" step seems stuck or takes several minutes.

**Possible Causes**:
- Large file size (>5MB)
- Complex Excel file with excessive formatting
- Slow internet connection
- Hidden sheets or macros in the file

**Solutions**:
1. Be patient - large files can take 30-60 seconds to parse
2. Don't refresh the page while parsing
3. Reduce file size by:
   - Removing unnecessary formatting (colors, borders, fonts)
   - Splitting into smaller batches (500-1000 products recommended)
   - Removing hidden sheets or macros
4. Check internet connection speed
5. Try uploading during off-peak hours
6. If parsing exceeds 2 minutes, refresh and try again

#### Preview Shows No Products

**Problem**: After parsing, the preview table is empty or shows 0 products.

**Possible Causes**:
- Excel file has no data rows (only headers)
- Data doesn't start in row 2
- All cells are empty or contain only whitespace
- File is password protected

**Solutions**:
1. Open your Excel file and verify it contains data rows
2. Ensure data starts in row 2 (row 1 should be headers)
3. Check that cells aren't empty or contain only spaces
4. Remove password protection from the file
5. Re-download the template and copy your data to the new file
6. Verify you're uploading the correct file

#### All Products Show as Invalid

**Problem**: Every product in the preview has validation errors.

**Possible Causes**:
- Missing required columns (SKU, Name, Category)
- Column names don't match template exactly
- Template structure was modified
- Data is in wrong columns

**Solutions**:
1. Verify all required columns exist: SKU, Name, Category
2. Check column names match the template exactly (case-sensitive)
3. Ensure you didn't add, remove, or rename columns
4. Verify data is in the correct columns
5. Re-download the template and transfer data carefully
6. Don't modify the template structure - only fill in data

### Validation Errors

#### Duplicate SKU Errors

**Problem**: You receive "Duplicate SKU" errors even though SKUs appear unique.

**Possible Causes**:
- Hidden characters or extra spaces in SKU cells
- Case sensitivity differences (SKUs are case-sensitive)
- SKU already exists in the database from a previous upload
- Similar SKUs that differ only in special characters

**Solutions**:
1. Check for extra spaces before or after SKUs
2. Verify case matches exactly (PROD-001 ≠ prod-001)
3. Use Excel's "Find Duplicates" feature to identify issues
4. Copy SKUs to Notepad and back to remove hidden characters
5. Search for the SKU in the product list to see if it already exists
6. Use unique SKUs for new products

#### Invalid Category Errors

**Problem**: Categories show as invalid even though you used the dropdown.

**Possible Causes**:
- Category name was edited after selection from dropdown
- Categories sheet was modified or deleted
- Extra spaces before or after category name
- Category list is outdated

**Solutions**:
1. Re-download the template to get the latest category list
2. Use the category dropdown again - don't type manually
3. Ensure you didn't edit the category after selecting it
4. Check that the "Categories" sheet is still present in the template
5. Remove any extra spaces before or after the category name
6. Try using the full category hierarchy path instead of just the name
7. Contact administrator if categories seem outdated

#### Invalid Price or Cost Errors

**Problem**: Prices or costs are not recognized as valid numbers.

**Possible Causes**:
- Currency symbols ($, €, £) included in the value
- Commas used as thousands separators
- Comma used instead of decimal point
- Cell formatted as text instead of number
- Hidden characters in the cell

**Solutions**:
1. Remove all currency symbols: change "$99.99" to "99.99"
2. Remove commas: change "1,000.00" to "1000.00"
3. Use decimal point (.) not comma (,): "99.99" not "99,99"
4. Format cells as "Number" in Excel (not "Text")
5. Copy values to Notepad and back to remove hidden characters
6. Re-enter the number manually if issues persist

#### Missing Required Field Errors

**Problem**: You receive "Missing required field" errors for fields that appear filled.

**Possible Causes**:
- Cells contain only whitespace (spaces, tabs)
- Cells appear filled but are actually empty
- Formula cells that evaluate to empty
- Hidden characters

**Solutions**:
1. Click on the cell and verify it contains actual data
2. Remove any extra spaces before or after the value
3. If using formulas, ensure they don't evaluate to empty
4. Copy data to Notepad and back to remove hidden characters
5. Re-type the value manually
6. Check that the cell isn't just formatted to look filled

### Batch and Product Management Issues

#### Batch Not Appearing in List

**Problem**: You uploaded a batch successfully but it doesn't appear in your batch list.

**Possible Causes**:
- Page needs to be refreshed
- Viewing wrong organization filter
- Batch creation actually failed despite success message
- Browser cache issue

**Solutions**:
1. Refresh the batches page (F5 or Ctrl+R)
2. Check that you're viewing the correct organization
3. Wait a few moments and refresh again
4. Clear browser cache and reload the page
5. Verify the batch number from the success screen
6. Contact support if batch is missing after 5 minutes

#### Cannot Download Batch Excel File

**Problem**: Clicking "Download Excel" doesn't start the download or fails.

**Possible Causes**:
- Browser blocking downloads or pop-ups
- Insufficient disk space
- Network connectivity issues
- File generation error on server

**Solutions**:
1. Check browser settings allow downloads from this site
2. Disable pop-up blockers for the Vendor Portal
3. Verify you have sufficient disk space
4. Try a different browser
5. Check internet connection
6. Wait a moment and try again
7. Contact support if issue persists

#### Product Status Not Updating

**Problem**: Product status doesn't change after batch approval/rejection.

**Possible Causes**:
- Page needs to be refreshed
- Status update is processing
- Synchronization delay

**Solutions**:
1. Refresh the page to see updated status
2. Wait 1-2 minutes for status to propagate
3. Check the batch detail page for current status
4. Clear browser cache if status still doesn't update
5. Contact administrator if status remains incorrect after 10 minutes

### Category and Attribute Issues

#### Categories Not Loading in Template Builder

**Problem**: Category tree doesn't load or appears empty in the template builder.

**Possible Causes**:
- Categories haven't been synced
- Network connectivity issues
- Browser cache issue
- Permission issues

**Solutions**:
1. Refresh the page
2. Check internet connection
3. Clear browser cache and reload
4. Contact administrator to sync categories
5. Try a different browser
6. Verify you have permission to access categories

#### Attributes Not Showing in Template

**Problem**: Expected attributes don't appear in the template builder or downloaded template.

**Possible Causes**:
- Attributes not assigned to your user or organization
- Attribute groups not configured
- Attributes not synced
- Permission issues

**Solutions**:
1. Contact administrator to verify attribute assignments
2. Check that attribute groups are assigned to your organization
3. Ask administrator to sync attributes
4. Verify you have permission to access attributes
5. Try selecting a different category (attributes may be category-specific)

### Notification Issues

#### Not Receiving Notifications

**Problem**: You don't receive notifications for batch status changes or other events.

**Possible Causes**:
- Notifications disabled in preferences
- WebSocket connection not established
- Browser blocking WebSocket connections
- Network firewall blocking connections

**Solutions**:
1. Check notification preferences in Settings
2. Enable notifications for the event types you want
3. Refresh the page to re-establish WebSocket connection
4. Check browser console for WebSocket errors
5. Verify your network/firewall allows WebSocket connections
6. Try a different browser or network
7. Contact IT support if corporate firewall is blocking connections

#### Notification Badge Not Updating

**Problem**: Notification badge doesn't show new notifications or count is incorrect.

**Possible Causes**:
- Page needs to be refreshed
- WebSocket connection dropped
- Browser cache issue

**Solutions**:
1. Click the notification bell icon to refresh
2. Refresh the entire page
3. Clear browser cache and reload
4. Check internet connection
5. Sign out and sign in again

### Performance Issues

#### Page Loading Slowly

**Problem**: Pages take a long time to load or appear unresponsive.

**Possible Causes**:
- Slow internet connection
- Large amount of data being loaded
- Browser performance issues
- Server performance issues

**Solutions**:
1. Check your internet connection speed
2. Close unnecessary browser tabs
3. Clear browser cache and cookies
4. Disable browser extensions temporarily
5. Try a different browser
6. Use filters to reduce the amount of data loaded
7. Contact support if issue persists across all pages

#### Upload or Download Very Slow

**Problem**: File uploads or downloads are extremely slow.

**Possible Causes**:
- Slow internet connection
- Large file size
- Network congestion
- Server load

**Solutions**:
1. Check your internet connection speed
2. Reduce file size by splitting into smaller batches
3. Try uploading/downloading during off-peak hours
4. Close other applications using bandwidth
5. Try a wired connection instead of Wi-Fi
6. Contact IT support if network speed is consistently slow

## Frequently Asked Questions (FAQ)

### General Questions

**Q: What browsers are supported?**

A: The Vendor Portal supports modern browsers including:
- Google Chrome (recommended, version 90+)
- Mozilla Firefox (version 88+)
- Microsoft Edge (version 90+)
- Safari (version 14+)

For best performance, use the latest version of Chrome or Edge.

**Q: Can I use the Vendor Portal on mobile devices?**

A: While the Vendor Portal is accessible on mobile devices, it's optimized for desktop use. For the best experience, especially when uploading files and reviewing data, we recommend using a desktop or laptop computer.

**Q: How long does my session last?**

A: Your session typically lasts 60 minutes from your last activity. After that, you'll need to sign in again. Save your work frequently to avoid losing data.

**Q: Can I have multiple browser tabs open with the Vendor Portal?**

A: Yes, but be aware that signing out in one tab will sign you out in all tabs. Also, making changes in multiple tabs simultaneously may cause conflicts.

### Account and Access Questions

**Q: How do I get an account?**

A: Contact your administrator to request an account. They will create your account and assign you to the appropriate organization with the correct role.

**Q: How long does account approval take?**

A: Account approval typically takes 1-2 business days. You'll receive an email notification when your account is approved.

**Q: Can I change my email address?**

A: Contact your administrator to change your email address. You cannot change it yourself for security reasons.

**Q: What's the difference between Admin and Vendor roles?**

A: 
- **Admin**: Full system access including user management, batch approval, category/attribute management, and system configuration
- **Vendor User**: Can submit products, track batches, view their organization's products, and manage their profile

**Q: Can I belong to multiple organizations?**

A: No, each user account is associated with a single organization. If you need access to multiple organizations, you'll need separate accounts.

### Product Upload Questions

**Q: What file formats are supported for upload?**

A: Only Excel formats are supported: .xlsx (Excel 2007+) and .xls (Excel 97-2003). CSV files are not supported.

**Q: What's the maximum file size for upload?**

A: The maximum file size is 10MB. If your file exceeds this, split it into multiple smaller batches.

**Q: How many products can I upload at once?**

A: There's no strict limit, but we recommend batches of 500-1000 products for optimal performance. Larger batches may take longer to process.

**Q: Can I edit products after uploading?**

A: Once a batch is submitted, you cannot edit the products. If you need to make changes, contact your administrator or wait for the batch to be rejected, then resubmit with corrections.

**Q: What happens if my batch is rejected?**

A: You'll receive a notification with the rejection reason. Review the feedback, correct the issues in your Excel file, and upload a new batch.

**Q: Can I upload the same SKU multiple times?**

A: No, SKUs must be unique across the entire system. If you try to upload a SKU that already exists, you'll receive a validation error.

**Q: Do I need to use the template?**

A: Yes, you must use the template generated by the Template Builder. The template ensures your file has the correct structure and valid categories/attributes.

### Template Questions

**Q: How do I get a template?**

A: Use the Template Builder in the vendor portal:
1. Navigate to Template Builder
2. Select your product categories
3. Select required attributes
4. Download the generated template

**Q: Can I modify the template structure?**

A: No, never modify the template structure. Don't add, remove, or rename columns. Only fill in the data rows. Modifying the structure will cause validation errors.

**Q: Why are some attributes missing from my template?**

A: Attributes are assigned to users/organizations by administrators. If you need additional attributes, contact your administrator to request access.

**Q: Can I reuse a template for multiple uploads?**

A: Yes, you can reuse templates as long as the categories and attributes haven't changed. However, we recommend downloading a fresh template periodically to ensure you have the latest categories and attributes.

**Q: What's the "Categories" sheet in the template?**

A: The Categories sheet contains the list of valid categories for dropdown selection. Don't modify or delete this sheet, as it's required for category validation.

### Batch and Status Questions

**Q: How long does batch approval take?**

A: Approval time varies depending on administrator workload. Typical approval time is 1-3 business days. You'll receive a notification when your batch is approved or rejected.

**Q: Can I cancel a batch after submission?**

A: No, you cannot cancel a batch after submission. Contact your administrator if you need to withdraw a batch.

**Q: What does "Pending" status mean?**

A: Pending means your batch is awaiting administrator review. No action is required from you at this stage.

**Q: What does "Approved" status mean?**

A: Approved means your batch has been reviewed and accepted by an administrator. The products are now ready for synchronization.

**Q: What does "Rejected" status mean?**

A: Rejected means your batch was reviewed and not accepted. Check the rejection reason, correct the issues, and submit a new batch.

**Q: Can I see who approved or rejected my batch?**

A: The batch timeline shows which administrator made the decision and when, but this information may not be visible to all vendor users depending on system configuration.

### Category and Attribute Questions

**Q: How do I know which category to use?**

A: Use the category dropdown in the template to see all available categories. Select the most specific category that matches your product. If unsure, contact your administrator for guidance.

**Q: Can I request new categories?**

A: Categories are managed by administrators. Contact your administrator to request new categories.

**Q: What are attribute groups?**

A: Attribute groups are collections of related attributes (e.g., "Apparel Attributes" might include Color, Size, Material). Your administrator assigns attribute groups to your organization to control which attributes you can use.

**Q: Are all attributes required?**

A: No, only attributes marked with an asterisk (*) in the template are required. Optional attributes can be left empty if not applicable to your product.

**Q: Can I add custom attributes?**

A: No, you can only use attributes that exist in the system and are assigned to your organization. Contact your administrator to request new attributes.

### Notification Questions

**Q: What types of notifications will I receive?**

A: Vendors receive notifications for:
- Batch status changes (approved/rejected)
- Upload progress and completion
- System announcements

Admins receive additional notifications for:
- New batch submissions
- Product sync completions
- System alerts

**Q: Can I disable notifications?**

A: Yes, you can configure notification preferences in your Settings. You can enable or disable specific notification types.

**Q: Why don't I see notifications in real-time?**

A: Real-time notifications require a WebSocket connection. If you're not receiving real-time notifications, check your network connection and browser settings. Refresh the page to re-establish the connection.

**Q: How long are notifications stored?**

A: Notifications are stored indefinitely in your notification history. You can mark them as read or clear them individually.

### Data and Security Questions

**Q: Is my data secure?**

A: Yes, the Vendor Portal uses industry-standard security practices including:
- HTTPS encryption for all data transmission
- JWT token-based authentication
- Password hashing with PBKDF2-HMAC-SHA256
- Role-based access control
- Secure database storage

**Q: Can other vendors see my products?**

A: No, vendors can only see their own organization's products. Administrators can see all products across all organizations.

**Q: What happens to my data if my account is deactivated?**

A: Your data (products, batches) remains in the system even if your account is deactivated. Contact your administrator if you need access to your data.

**Q: Can I export my product data?**

A: Yes, you can download batch Excel files which contain your product data. Administrators can also export product data for you if needed.

### Product Sync Questions

**Q: What is the product sync system?**

A: The system is where approved products are synchronized for final publication and distribution.

**Q: When do my products sync?**

A: Products are eligible for sync after batch approval. Administrators control when and how products are synced.

**Q: Can I see if my products have been synced?**

A: Product sync status may be visible in the product detail view, depending on system configuration. Contact your administrator for sync status information.

**Q: What if my product fails to sync?**

A: Administrators monitor sync failures and will work to resolve issues. You may be contacted if product data needs to be corrected.

## Error Messages Reference

### Authentication Errors

| Error Message | Meaning | Solution |
|--------------|---------|----------|
| Invalid Credentials | Email or password is incorrect | Verify credentials, use forgot password |
| Account Pending Approval | Account not yet approved | Wait for admin approval |
| Account Inactive | Account has been deactivated | Contact administrator |
| Token Expired | Session has timed out | Sign in again |
| Invalid Token | Authentication token is invalid | Clear cache, sign in again |
| Access Denied | Insufficient permissions | Contact administrator |

### Upload Errors

| Error Message | Meaning | Solution |
|--------------|---------|----------|
| File size exceeds 10MB | File is too large | Reduce file size or split into batches |
| Invalid file format | File is not .xlsx or .xls | Save as Excel format |
| File is corrupted | File cannot be read | Try opening in Excel, re-save |
| Missing required field: [field] | Required field is empty | Fill in the required field |
| Duplicate SKU '[sku]' in upload | SKU appears multiple times in file | Ensure each SKU is unique |
| Product with SKU '[sku]' already exists | SKU already in database | Use a different SKU |
| Invalid category: '[category]' | Category doesn't exist or is misspelled | Use category dropdown in template |
| Invalid price value: [value] | Price is not a valid number | Remove symbols, use numbers only |
| Unknown attribute: [attribute] | Attribute doesn't exist | Use only attributes from template |

### System Errors

| Error Message | Meaning | Solution |
|--------------|---------|----------|
| Network Error | Connection to server failed | Check internet connection, try again |
| Server Error | Internal server error | Wait a moment, try again, contact support |
| Request Timeout | Request took too long | Check connection, try again |
| Service Unavailable | System is temporarily down | Wait and try again later |

## System Requirements

### Browser Requirements

**Minimum Requirements**:
- Modern browser released within the last 2 years
- JavaScript enabled
- Cookies and local storage enabled
- Pop-ups allowed for the Vendor Portal domain

**Recommended Browsers**:
- Google Chrome 90+ (recommended)
- Microsoft Edge 90+
- Mozilla Firefox 88+
- Safari 14+

### Network Requirements

- Stable internet connection (minimum 1 Mbps)
- WebSocket support for real-time notifications
- HTTPS access (port 443)
- No proxy or firewall blocking WebSocket connections

### Software Requirements

- Microsoft Excel 2007+ or compatible spreadsheet software for template editing
- PDF reader for viewing documentation (optional)

### Hardware Requirements

- Minimum 4GB RAM
- Modern processor (Intel i3 or equivalent)
- Sufficient disk space for downloaded files

## Getting Additional Support

### Before Contacting Support

1. Check this troubleshooting guide for solutions
2. Try the suggested solutions for your issue
3. Clear browser cache and cookies
4. Try a different browser
5. Gather information about your issue:
   - What were you trying to do?
   - What happened instead?
   - Any error messages you received
   - Your browser and operating system
   - Steps to reproduce the issue

### How to Report Issues

When contacting support, please include:

1. **Your Information**:
   - Your name and email address
   - Your organization name
   - Your user role (Admin or Vendor)

2. **Issue Details**:
   - Clear description of the problem
   - What you were trying to accomplish
   - What happened instead
   - When the issue started

3. **Error Information**:
   - Exact error message text
   - Screenshot of the error (if possible)
   - Browser console errors (if technical)

4. **Environment Information**:
   - Browser name and version
   - Operating system
   - Network type (office, home, mobile)

5. **Steps to Reproduce**:
   - Step-by-step instructions to recreate the issue
   - Whether the issue happens every time or intermittently

### Support Contact Information

**Email Support**: [Insert support email address]

**Support Hours**: [Insert support hours]

**Response Time**: 
- Critical issues: Within 4 hours
- High priority: Within 1 business day
- Normal priority: Within 2 business days

**Emergency Contact**: [Insert emergency contact for critical system issues]

### Escalation Process

If your issue is not resolved:

1. **Level 1**: Initial support contact
2. **Level 2**: Escalate to senior support after 2 business days
3. **Level 3**: Escalate to system administrator or technical team

### Feature Requests

Have an idea for improving the Vendor Portal?

- Submit feature requests to: [Insert feature request email/form]
- Include a clear description of the desired feature
- Explain the business value or problem it would solve
- Provide examples or use cases

Feature requests are reviewed quarterly and prioritized based on user needs and system roadmap.

## Related Topics

### Getting Started
- **Admin Getting Started** - Admin user guide and first steps
- **[Vendor Getting Started](../vendor/getting-started.md)** - Vendor user guide and first steps

### Admin Documentation
- **Admin Dashboard** - Dashboard troubleshooting
- **Admin Batch Management** - Batch review troubleshooting
- **Admin Product Management** - Product sync troubleshooting
- **Admin Category Management** - Category sync troubleshooting

### Vendor Documentation
- **[Vendor Product Upload](../vendor/product-upload.md)** - Upload and validation troubleshooting
- **[Vendor Batch Tracking](../vendor/batch-tracking.md)** - Batch tracking troubleshooting
- **[Vendor Template Builder](../vendor/template-builder.md)** - Template troubleshooting

### Common Documentation
- **[Authentication](./authentication.md)** - Sign-in and session troubleshooting
- **[Notifications System](./notifications-system.md)** - Notification troubleshooting

---

**Back to**: [Home](../README.md)

## Document Version

**Last Updated**: [Current Date]
**Version**: 1.0
**Maintained By**: [Team/Department Name]

This document is regularly updated based on user feedback and system changes. If you notice outdated information, please contact support.
