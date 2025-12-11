# Product Upload

**Navigation**: [Home](../README.md) > [Vendor Documentation](./README.md) > Product Upload

## Overview

The Product Upload feature allows you to submit multiple products at once using Excel files. The upload process includes file validation, data preview, and error checking to ensure your products meet all requirements before submission. Once uploaded, your products are grouped into a batch and sent to administrators for review and approval.

The upload wizard guides you through each step, providing real-time feedback on data quality and validation errors, helping you submit accurate product information efficiently.

## Key Concepts

**Batch**: A collection of products uploaded together via a single Excel file. Each batch is assigned a unique batch number and tracked through the approval process.

**Upload Wizard**: A step-by-step interface that guides you through file selection, validation, preview, and confirmation.

**Validation**: Automated checks that verify your product data meets all requirements (required fields, data formats, unique SKUs, valid categories).

**Preview**: A review screen showing all products from your file with validation status before final submission.

**File Size Limit**: Maximum file size of 10MB to ensure optimal processing performance.

**Preview Limit**: Maximum of 1,000 rows displayed in preview for performance optimization (larger files are still processed).

## Complete Upload Workflow

### Prerequisites

- Active vendor account with an assigned organization
- Completed Excel template with product data
- Valid product information (unique SKUs, valid categories, required fields filled)
- File size under 10MB
- Microsoft Excel or compatible spreadsheet software

### Step 1: Navigate to Upload Page

1. **Access Upload Page**
   - From the vendor dashboard, click "Upload Products" in the sidebar navigation
   - Or navigate directly to the Upload section from the main menu

2. **Review Upload Requirements**
   - The upload page displays file requirements and limitations
   - Supported formats: Excel (.xlsx, .xls)
   - Maximum file size: 10MB
   - Preview limited to 1,000 rows

### Step 2: Select and Upload File

1. **Choose Your File**
   - Click the upload area or drag and drop your Excel file
   - The system accepts only .xlsx and .xls file formats
   - File size is validated immediately (must be under 10MB)

2. **File Validation**
   - The system performs initial validation:
     - File type check (must be Excel format)
     - File size check (must be under 10MB)
     - File readability check
   - If validation fails, an error message explains the issue
   - Fix the issue and try uploading again

3. **View Selected File**
   - Once selected, the file information is displayed:
     - File name
     - File size in MB
   - Review the information to ensure you selected the correct file

4. **Start Parsing**
   - Click the "Preview Upload" button to begin file processing
   - The system parses your Excel file and extracts product data
   - A loading indicator shows parsing progress
   - Parsing typically takes a few seconds depending on file size

### Step 3: Review Preview Data

After parsing completes, the preview screen displays your products with validation results.

#### Preview Summary Statistics

The top of the preview shows three key metrics:

- **Total Products**: Total number of products found in your file
- **Valid Products**: Number of products that passed all validation checks (shown in green)
- **Invalid Products**: Number of products with validation errors (shown in red)

#### Preview Table

The preview table displays all products with the following columns:

- **Status**: Visual indicator (green checkmark for valid, red X for invalid)
- **SKU**: Product SKU with validation errors displayed below if present
- **Name**: Product name
- **Category**: Product category
- **Price**: Product selling price
- **Cost**: Product cost price
- **Attributes**: First 3 custom attributes (with "+X more" badge if additional attributes exist)

#### Validation Error Display

Products with validation errors are highlighted:

- **Row Background**: Light red background for invalid products
- **Error Messages**: Displayed below the SKU in red text
- **Error Types**: Specific error messages explain what needs to be fixed

#### File-Level Errors

If the entire file has issues, they appear in a red alert box above the table:

- Missing required columns
- File format issues
- Parsing errors
- Other file-level problems

### Step 4: Handle Validation Errors

If your preview shows invalid products, you must fix the errors before proceeding.

#### Common Validation Errors

**Missing Required Fields**
- Error: "Missing required field: [field_name]"
- Solution: Fill in all required fields (SKU, Name, Category)
- Required fields cannot be empty or contain only whitespace

**Duplicate SKU in Upload**
- Error: "Duplicate SKU '[sku]' in upload (also in row [number])"
- Solution: Ensure each SKU is unique within your file
- Check for accidental duplicates or copy-paste errors

**Duplicate SKU in Database**
- Error: "Product with SKU '[sku]' already exists in database"
- Solution: Use a different SKU or update the existing product instead
- SKUs must be unique across all products in the system

**Invalid Category**
- Error: "Invalid category: '[category_name]'. Please select from available categories."
- Solution: Use the category dropdown in your template to select a valid category
- Category names are case-insensitive but must match exactly
- Ensure you didn't modify the category name after selection

**Invalid Price or Cost**
- Error: "Invalid price value: [value]" or "Invalid cost value: [value]"
- Solution: Enter numeric values only (e.g., "99.99" not "$99.99")
- Remove currency symbols, commas, or other formatting
- Use decimal points (.) not commas (,) for decimal numbers

**Unknown Attribute**
- Error: "Unknown attribute: [attribute_name]"
- Solution: Ensure the attribute exists in the system
- Use only attributes from your downloaded template
- Don't add custom columns that aren't in the template

#### Fixing Validation Errors

1. **Note the Errors**
   - Review all validation errors in the preview
   - Take note of row numbers and specific error messages
   - Identify patterns (e.g., multiple products with the same issue)

2. **Cancel Upload**
   - Click the "Cancel" button to return to the upload screen
   - Your file is not submitted when you cancel

3. **Update Your Excel File**
   - Open your original Excel file
   - Fix all identified errors based on the error messages
   - Double-check your corrections
   - Save the updated file

4. **Re-upload**
   - Upload the corrected file
   - Review the new preview to verify all errors are fixed
   - Repeat until all products are valid

### Step 5: Confirm and Create Batch

Once all products are valid, you can create the batch.

1. **Review Valid Products**
   - Verify all products show green checkmarks
   - Spot-check a few products to ensure data accuracy
   - Confirm the total product count is correct

2. **Confirm Upload**
   - Click the "Confirm & Create Batch" button
   - The button is only enabled when all products are valid
   - A loading indicator shows batch creation progress

3. **Batch Creation**
   - The system creates a new batch record
   - All products are created and linked to the batch
   - Products are assigned "pending" status
   - The batch is submitted for administrator review

4. **View Completion**
   - A success screen displays batch information:
     - Batch Number: Unique identifier for tracking
     - Filename: Your uploaded file name
     - Product Count: Number of products in the batch
     - Status: Current batch status (typically "pending")

### Step 6: Next Steps

After successful upload:

1. **Upload Another File** (optional)
   - Click "Upload Another File" to start a new upload
   - Useful for uploading multiple batches of different product types

2. **View My Batches**
   - Click "View My Batches" to see all your batches
   - Track the approval status of your uploaded batch
   - View detailed batch information and timeline

3. **Monitor Notifications**
   - Watch for notifications about batch status changes
   - You'll be notified when your batch is approved or rejected
   - Notifications appear in the notification center (bell icon)

## Data Format Requirements

### Required Fields

Every product must include these fields:

- **SKU**: Unique product identifier
  - Must be unique across all products in the system
  - Cannot be empty or whitespace only
  - Recommended format: alphanumeric with hyphens or underscores
  - Example: "PROD-001", "SKU_12345"

- **Name**: Product name
  - Cannot be empty or whitespace only
  - Should be descriptive and clear
  - Recommended length: 10-100 characters
  - Example: "Wireless Bluetooth Headphones"

- **Category**: Product category
  - Must match an existing category in the system
  - Use the dropdown in your template to ensure validity
  - Case-insensitive but must match exactly
  - Can be category name or full hierarchy path
  - Example: "Electronics" or "Electronics > Audio > Headphones"

### Optional Fields

These fields are optional but recommended:

- **Description**: Product description
  - Provides additional product details
  - Can be empty
  - Recommended length: 50-500 characters
  - Avoid special characters that might cause issues

- **Price**: Selling price
  - Must be a valid decimal number if provided
  - No currency symbols or commas
  - Use decimal point (.) for cents
  - Example: "99.99" not "$99.99" or "99,99"

- **Cost**: Cost price
  - Must be a valid decimal number if provided
  - Same format rules as Price
  - Example: "49.50"

### Custom Attributes

Additional attributes from your template:

- **Attribute Names**: Must match attribute keys from your template
- **Attribute Values**: Must match the attribute's data type
- **Required Attributes**: Marked with asterisk (*) in template must be filled
- **Optional Attributes**: Can be left empty if not applicable

### Data Type Formats

**Text Fields**
- Any alphanumeric characters
- Avoid special characters: quotes, pipes (|), tabs, line breaks
- Use standard apostrophes (') not smart quotes (' ')
- Maximum length varies by field

**Numeric Fields**
- Numbers only (0-9)
- Decimal point (.) for fractional values
- No commas, currency symbols, or other formatting
- Negative numbers: use minus sign (-) prefix
- Example: "123.45" or "-10.50"

**Date Fields** (if applicable)
- ISO format: YYYY-MM-DD
- Example: "2024-03-15"
- Avoid regional formats (MM/DD/YYYY or DD/MM/YYYY)

**Boolean Fields** (if applicable)
- Use consistent values: "Yes/No", "True/False", or "1/0"
- Case-insensitive
- Don't mix formats within the same file

## Common Validation Rules

### SKU Validation

- **Uniqueness**: SKU must be unique across all products
- **Format**: Alphanumeric characters, hyphens, underscores allowed
- **Length**: Typically 3-50 characters
- **Case Sensitivity**: SKUs are case-sensitive ("PROD-001" ≠ "prod-001")

### Category Validation

- **Existence**: Category must exist in the system
- **Case Insensitive**: "Electronics" = "electronics" = "ELECTRONICS"
- **Hierarchy Support**: Can use full path or just category name
- **Whitespace**: Leading/trailing whitespace is trimmed automatically

### Price and Cost Validation

- **Numeric Only**: Must be valid decimal numbers
- **Positive Values**: Typically must be positive (≥ 0)
- **Precision**: Up to 2 decimal places recommended
- **Range**: Must be reasonable (system may have min/max limits)

### Attribute Validation

- **Attribute Existence**: Attribute key must exist in the system
- **Data Type**: Value must match attribute's defined data type
- **Required Attributes**: Cannot be empty if marked as required
- **Value Length**: May have maximum length restrictions

## Fixing Validation Errors

### Step-by-Step Error Resolution

1. **Identify All Errors**
   - Review the preview table carefully
   - Note all products with red X status icons
   - Read each error message completely
   - Look for patterns across multiple products

2. **Prioritize Fixes**
   - Fix file-level errors first (missing columns, format issues)
   - Then fix required field errors (missing SKU, Name, Category)
   - Then fix data format errors (invalid prices, categories)
   - Finally fix attribute-specific errors

3. **Update Excel File**
   - Open your original Excel file
   - Navigate to the problematic rows
   - Make corrections based on error messages
   - Verify your changes are correct

4. **Validate Locally**
   - Double-check all required fields are filled
   - Verify all categories are from the dropdown
   - Check number formats (no symbols or commas)
   - Ensure SKUs are unique within the file

5. **Re-upload and Verify**
   - Upload the corrected file
   - Review the new preview
   - Verify all previous errors are resolved
   - Check that no new errors were introduced

### Error Resolution Examples

**Example 1: Missing Required Field**

Error Message:
```
Missing required field: name
```

Resolution:
1. Open Excel file
2. Find the row with the error (check row number in preview)
3. Fill in the Name column with a descriptive product name
4. Save the file
5. Re-upload

**Example 2: Duplicate SKU**

Error Message:
```
Duplicate SKU 'PROD-001' in upload (also in row 5)
```

Resolution:
1. Open Excel file
2. Find both rows with SKU "PROD-001"
3. Change one SKU to a unique value (e.g., "PROD-001A")
4. Verify no other duplicates exist
5. Save and re-upload

**Example 3: Invalid Category**

Error Message:
```
Invalid category: 'Electonics'. Please select from available categories.
```

Resolution:
1. Open Excel file
2. Find the row with the typo ("Electonics" should be "Electronics")
3. Click the Category cell
4. Select the correct category from the dropdown
5. Save and re-upload

**Example 4: Invalid Price Format**

Error Message:
```
Invalid price value: $99.99
```

Resolution:
1. Open Excel file
2. Find the row with the price error
3. Remove the dollar sign: change "$99.99" to "99.99"
4. Ensure the cell format is "Number" not "Text"
5. Save and re-upload

## Upload Performance Tips

### Optimizing File Size

1. **Remove Unnecessary Columns**: Only include attributes you need
2. **Limit Rows**: Upload in batches of 500-1000 products for best performance
3. **Compress Images**: If including image URLs, ensure they're optimized
4. **Remove Formatting**: Excessive cell formatting increases file size

### Batch Upload Strategy

1. **Group Similar Products**: Upload products with similar attributes together
2. **Test Small Batches First**: Upload 10-20 products to test your format
3. **Schedule Large Uploads**: Upload large batches during off-peak hours
4. **Split by Category**: Create separate uploads for different product categories

### Avoiding Common Mistakes

1. **Don't Modify Template Structure**: Never add, remove, or rename columns
2. **Use Dropdown for Categories**: Always select from dropdown, don't type
3. **Check SKU Uniqueness**: Verify SKUs are unique before uploading
4. **Validate Data Locally**: Review your data in Excel before uploading
5. **Save Backup Copies**: Keep a copy of your file before uploading

## Troubleshooting

### Upload Issues

**Issue**: File upload fails immediately

**Solutions**:
- Check file size (must be under 10MB)
- Verify file format (.xlsx or .xls only)
- Ensure file is not corrupted (try opening in Excel)
- Check internet connection
- Try a different browser
- Clear browser cache and cookies

**Issue**: Parsing takes a very long time

**Solutions**:
- Large files (>5MB) may take 30-60 seconds to parse
- Reduce file size by splitting into smaller batches
- Remove unnecessary formatting from Excel file
- Ensure file doesn't contain hidden sheets or macros
- Wait patiently - don't refresh the page

**Issue**: Preview shows no products

**Solutions**:
- Verify your Excel file has data rows (not just headers)
- Check that data starts in row 2 (row 1 should be headers)
- Ensure cells aren't empty or contain only whitespace
- Verify file isn't password protected
- Re-download template and copy data to new file

### Validation Issues

**Issue**: All products show as invalid

**Solutions**:
- Check for missing required columns (SKU, Name, Category)
- Verify column names match template exactly
- Ensure you didn't modify the template structure
- Check that data is in the correct columns
- Re-download template and transfer data carefully

**Issue**: Category validation fails for all products

**Solutions**:
- Verify you used the category dropdown in the template
- Check that categories haven't been modified after selection
- Ensure the Categories sheet is still present in the template
- Re-download template to get updated category list
- Contact administrator if categories seem outdated

**Issue**: SKU duplicates detected but SKUs look unique

**Solutions**:
- Check for hidden characters or extra spaces
- Verify case sensitivity (SKUs are case-sensitive)
- Look for similar SKUs that differ only in special characters
- Use Excel's "Find Duplicates" feature to identify issues
- Clean data by copying to Notepad and back to remove hidden characters

### Batch Creation Issues

**Issue**: "Confirm & Create Batch" button is disabled

**Solutions**:
- Ensure all products show green checkmarks (valid status)
- Fix any remaining validation errors
- Refresh the preview if you think errors are resolved
- Check for file-level errors at the top of the preview
- Cancel and re-upload if issues persist

**Issue**: Batch creation fails after confirmation

**Solutions**:
- Check internet connection
- Verify you're still logged in (session may have expired)
- Try uploading a smaller batch
- Check with administrator for system issues
- Review browser console for error messages
- Contact support if issue persists

**Issue**: Success screen shows but batch not in list

**Solutions**:
- Refresh the batches page
- Check that you're viewing the correct organization
- Verify batch was created by checking batch number
- Wait a few moments and refresh again
- Contact support if batch is missing after 5 minutes

### Data Format Issues

**Issue**: Numbers not recognized as valid

**Solutions**:
- Remove all formatting (currency symbols, commas, spaces)
- Use decimal point (.) not comma (,) for decimals
- Ensure cell format is "Number" not "Text" in Excel
- Check for hidden characters
- Re-enter the number manually

**Issue**: Categories not matching despite using dropdown

**Solutions**:
- Verify you didn't edit the category after selecting from dropdown
- Check that the Categories sheet wasn't modified
- Ensure no extra spaces before or after category name
- Re-download template to get latest categories
- Use full hierarchy path if simple name doesn't work

**Issue**: Special characters causing errors

**Solutions**:
- Remove or replace special characters: quotes, pipes (|), tabs
- Use standard apostrophes (') not smart quotes (' ')
- Avoid line breaks within cells
- Copy text to Notepad first to remove formatting
- Use HTML entities for special characters if needed

## Best Practices

### Before Upload

1. **Validate Data in Excel**: Review all data before uploading
2. **Check Required Fields**: Ensure all required fields are filled
3. **Verify SKU Uniqueness**: Use Excel's duplicate detection
4. **Test Categories**: Verify all categories are from dropdown
5. **Review Numbers**: Check price and cost formatting
6. **Backup Your File**: Save a copy before uploading

### During Upload

1. **Don't Refresh Page**: Wait for parsing to complete
2. **Review Preview Carefully**: Check all products before confirming
3. **Fix All Errors**: Don't skip validation errors
4. **Verify Counts**: Ensure product count matches expectations
5. **Double-Check Data**: Spot-check a few products for accuracy

### After Upload

1. **Note Batch Number**: Record the batch number for tracking
2. **Monitor Notifications**: Watch for approval/rejection notifications
3. **Track Status**: Check batch status regularly
4. **Respond to Feedback**: Address any rejection feedback promptly
5. **Keep Records**: Maintain copies of uploaded files for reference

### Data Quality

1. **Consistent Formatting**: Use the same format for similar data
2. **Complete Information**: Fill in as many fields as possible
3. **Accurate Categories**: Select the most specific category available
4. **Descriptive Names**: Use clear, descriptive product names
5. **Reasonable Prices**: Ensure prices and costs are realistic
6. **Quality Descriptions**: Write informative product descriptions

## Related Topics

### Before Uploading
- **[Template Builder](./template-builder.md)** - Create customized Excel templates for upload
- **[Getting Started](./getting-started.md)** - Quick start guide for new vendors

### After Uploading
- **[Batch Tracking](./batch-tracking.md)** - Track the status of your uploaded batches
- **[Product Management](./product-management.md)** - Manage your submitted products
- **[Dashboard](./dashboard.md)** - View your product statistics and recent activity

### System Features
- **[Notifications](./notifications.md)** - Receive upload progress notifications
- **[Settings](./settings.md)** - Update profile and preferences

### Common Documentation
- **[Troubleshooting](../common/troubleshooting.md)** - Solutions for upload and validation issues

### Understanding Admin Workflow
- **Admin Batch Management** - How admins review your uploads
- **Admin Category Management** - How categories are managed

---

**Back to**: [Vendor Documentation](./README.md) | [Home](../README.md)
