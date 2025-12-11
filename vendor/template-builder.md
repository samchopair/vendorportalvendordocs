# Template Builder

**Navigation**: [Home](../README.md) > [Vendor Documentation](./README.md) > Template Builder

## Overview

The Template Builder is a powerful tool that allows you to create customized Excel templates for bulk product uploads. By selecting the specific attributes you need, you can generate a template that includes all required product columns plus any additional custom attributes relevant to your products.

The generated template includes data validation features, such as category dropdowns, to help ensure data accuracy and reduce upload errors.

## Key Concepts

**Excel Template**: A pre-formatted Excel file with column headers that match the system's expected product data structure. Templates include data validation rules to guide data entry.

**Required Columns**: Standard product fields that are always included in every template (SKU, Name, Category, Description, Price, Cost).

**Custom Attributes**: Additional product characteristics specific to your business needs (e.g., Color, Size, Material, Brand).

**Attribute Groups**: Collections of related attributes organized by category or purpose. Your administrator assigns which attribute groups you can access.

**Category Dropdown**: A data validation feature in the Category column that provides a dropdown list of all available categories, including child categories with their full hierarchy path.

**Protected Headers**: The header row in the template is locked to prevent accidental modification, while data rows remain fully editable.

## How to Build and Download a Template

### Prerequisites

- Active vendor account with assigned attribute groups
- Permission to access the Template Builder
- Microsoft Excel or compatible spreadsheet software

### Steps

1. **Navigate to Template Builder**
   - From the vendor dashboard, click on "Build Template" in the sidebar navigation
   - Or access it directly from the main navigation menu

2. **Review Required Columns**
   - The "Required Product Columns" section shows all standard fields that will be included in your template
   - These columns are always present and cannot be deselected:
     - **SKU**: Unique product identifier (required)
     - **Name**: Product name (required)
     - **Category**: Product category with dropdown validation (required)
     - **Description**: Product description (optional)
     - **Price**: Selling price (optional)
     - **Cost**: Cost price (optional)
   - The Category column will include dropdown validation with all available categories

3. **Search for Attributes (Optional)**
   - Use the search bar to quickly find specific attribute groups or attributes
   - Search works across both group names and individual attribute names
   - Clear the search to see all available attribute groups

4. **Select Custom Attributes**
   - Browse through the available attribute groups
   - Click on a group card to expand and view its attributes
   - Each group shows:
     - Group name and visibility badge (Public or Vendor-Specific)
     - Number of attributes in the group
   - Check the boxes next to attributes you want to include in your template
   - Attributes marked with a red asterisk (*) are required fields
   - Each attribute displays its data type (Text, Number, Date, etc.)

5. **Review Template Summary**
   - The right sidebar shows your template summary:
     - **Required Columns**: Lists all standard product fields
     - **Additional Attributes**: Shows your selected custom attributes with count
     - **Total Columns**: Displays the total number of columns in your template
   - Verify your selections before downloading

6. **Download Template**
   - Click the "Download Template" button in the summary panel
   - The system generates your customized Excel file
   - The file downloads automatically to your default downloads folder
   - File name format: `product_template_[timestamp].xlsx`

## Understanding Template Structure

### Workbook Sheets

Your downloaded template contains two sheets:

1. **Products Sheet** (visible)
   - Main sheet where you enter product data
   - Contains all selected columns with formatted headers
   - Header row is protected (read-only) to prevent accidental changes
   - Data rows (rows 2-1001) are fully editable
   - Category column includes dropdown validation
   - Columns are pre-sized for readability but can be resized as needed

2. **Categories Sheet** (hidden)
   - Contains the list of all available categories for dropdown validation
   - Shows category hierarchy (e.g., "Electronics > Computers > Laptops")
   - This sheet is hidden and should not be modified
   - Used by the Category column dropdown validation

### Header Row Protection

The template includes header row protection to prevent accidental modifications:

- **Header Row (Row 1)**: Locked and read-only
  - Styled with bold font and gray background
  - Cannot be edited, deleted, or modified
  - Ensures column names match system expectations

- **Data Rows (Rows 2-1001)**: Fully editable
  - Enter your product data in these rows
  - All cells are unlocked and can be modified
  - Supports up to 1,000 products per template

- **Column Resizing**: Allowed
  - You can adjust column widths as needed
  - Columns are pre-sized but can be customized

### Category Dropdown Validation

The Category column includes special data validation:

- **Dropdown List**: Click the cell to see available categories
- **Hierarchy Display**: Categories show their full path (e.g., "Home & Garden > Furniture > Chairs")
- **Error Prevention**: Only valid categories from the dropdown can be entered
- **Error Message**: If you type an invalid category, you'll see: "Invalid Category - Please select a category from the dropdown"
- **Child Categories**: All child categories are included in the dropdown with their parent path for easy identification

### Column Types

Understanding column data types helps ensure proper data entry:

- **Text**: Any alphanumeric characters (e.g., SKU, Name, Description)
- **Number**: Numeric values only (e.g., Price, Cost, Quantity)
- **Date**: Date values in standard format (e.g., YYYY-MM-DD)
- **Boolean**: True/False or Yes/No values
- **Dropdown**: Select from predefined options (Category column)

## Template Best Practices

### Before Downloading

1. **Select Relevant Attributes**: Only include attributes you'll actually use to keep your template manageable
2. **Review Requirements**: Note which attributes are marked as required (red asterisk)
3. **Plan Your Data**: Ensure you have the necessary product information before starting data entry

### Data Entry Guidelines

1. **Required Fields**: Always fill in fields marked with an asterisk (*)
2. **Category Selection**: Always use the dropdown to select categories - don't type them manually
3. **Data Consistency**: Use consistent formatting for similar data (e.g., always use "Yes/No" or "True/False", not mixed)
4. **SKU Uniqueness**: Ensure each SKU is unique across all your products
5. **Number Formats**: Enter numbers without currency symbols or commas (e.g., "99.99" not "$99.99")
6. **Empty Cells**: Leave optional fields empty if you don't have the data - don't use "N/A" or similar placeholders
7. **Text Length**: Keep descriptions concise but informative
8. **Special Characters**: Avoid special characters that might cause issues (e.g., quotes, pipes, tabs)

### File Management

1. **Save Regularly**: Save your work frequently while entering data
2. **Backup Copies**: Keep backup copies of completed templates before uploading
3. **Version Control**: Use descriptive file names if you maintain multiple versions (e.g., "products_electronics_v2.xlsx")
4. **Don't Modify Structure**: Never add, remove, or rename columns - this will cause upload errors
5. **Keep Headers Protected**: Don't attempt to unlock or modify the header row

### Data Validation

Before uploading your completed template:

1. **Check Required Fields**: Verify all required fields are filled in
2. **Validate Categories**: Ensure all categories are selected from the dropdown
3. **Review Numbers**: Check that prices and costs are reasonable and properly formatted
4. **Verify SKUs**: Confirm all SKUs are unique and follow your naming convention
5. **Test Small Batch**: Consider uploading a small test batch first to verify your data format

## Common Issues and Solutions

### Template Download Issues

**Issue**: Template download fails or doesn't start

**Solutions**:
- Check your internet connection
- Ensure pop-up blockers aren't preventing the download
- Try a different browser
- Clear browser cache and try again
- Contact support if the issue persists

**Issue**: No attribute groups available

**Solutions**:
- Contact your administrator to assign attribute groups to your account
- Verify you're logged in with the correct vendor account
- Check that your account is active and approved

### Template Usage Issues

**Issue**: Cannot edit cells in the template

**Solutions**:
- Ensure you're editing data rows (row 2 and below), not the header row
- Check that the file isn't opened in read-only mode
- Verify you have write permissions to the file location
- Try opening the file in a different spreadsheet application

**Issue**: Category dropdown not working

**Solutions**:
- Ensure you're clicking in the Category column (Column C)
- Don't type the category - click the dropdown arrow or press Alt+Down Arrow
- Verify the template hasn't been modified (re-download if needed)
- Check that the Categories sheet is still present (it should be hidden)

**Issue**: "Invalid Category" error when uploading

**Solutions**:
- Always select categories from the dropdown - don't type them manually
- Ensure you haven't modified the Categories sheet
- Re-download the template if categories seem outdated
- Verify the category still exists in the system

**Issue**: Header row accidentally modified

**Solutions**:
- Re-download a fresh template
- Do not attempt to fix modified headers manually
- Copy your data to a new template with correct headers

### Data Entry Issues

**Issue**: Excel shows validation errors for numbers

**Solutions**:
- Remove currency symbols, commas, and other formatting
- Use decimal points (.) not commas (,) for decimal numbers
- Ensure the cell format is set to "Number" not "Text"

**Issue**: Special characters causing problems

**Solutions**:
- Avoid using quotes, pipes (|), tabs, or line breaks in text fields
- Use standard apostrophes (') instead of smart quotes (' ')
- Remove any hidden characters by copying text to Notepad first

**Issue**: Date format not recognized

**Solutions**:
- Use ISO format: YYYY-MM-DD (e.g., 2024-03-15)
- Ensure the cell format is set to "Date"
- Avoid regional date formats that might be ambiguous

## Tips for Efficient Template Use

### Organizing Your Work

1. **Create Category-Specific Templates**: Build separate templates for different product categories to keep attribute selection focused
2. **Reuse Templates**: Save completed templates as masters for future uploads of similar products
3. **Batch Similar Products**: Group products with similar attributes together in the same upload

### Maximizing Accuracy

1. **Use Dropdown Validation**: Always use the category dropdown to avoid typos and ensure valid selections
2. **Copy-Paste Carefully**: When copying data from other sources, paste as "Values Only" to avoid formatting issues
3. **Double-Check Required Fields**: Before uploading, sort or filter to find any empty required fields
4. **Validate Before Upload**: Use Excel's data validation features to check for errors before uploading

### Collaboration

1. **Share Templates**: Share your customized templates with team members who upload similar products
2. **Document Conventions**: Create a guide for your team on how to fill in specific attributes consistently
3. **Review Process**: Have someone review completed templates before uploading to catch errors

## Next Steps

After building and completing your template:

1. **Fill in Product Data**: Enter your product information following the best practices above
2. **Save Your Work**: Save the completed template to your computer
3. **Upload Products**: Navigate to the Upload page to submit your products
4. **Track Progress**: Monitor your batch status in the Batch Tracking section

## Related Topics

### Next Steps
- **[Product Upload](./product-upload.md)** - Learn how to upload your completed template
- **[Batch Tracking](./batch-tracking.md)** - Track the status of your uploaded batches
- **[Product Management](./product-management.md)** - Manage your submitted products

### Understanding Templates
- **[Getting Started](./getting-started.md)** - Quick start guide for first-time users
- **[Dashboard](./dashboard.md)** - View your product statistics and recent activity

### Configuration & Attributes
- **Admin Attribute Management** - How attributes are created and organized
- **Admin Category Management** - How categories are managed

### Common Documentation
- **[Troubleshooting](../common/troubleshooting.md)** - Solutions for template and upload issues

---

**Back to**: [Vendor Documentation](./README.md) | [Home](../README.md)

