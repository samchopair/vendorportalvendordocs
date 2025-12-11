# Product Management

**Navigation**: [Home](../README.md) > [Vendor Documentation](./README.md) > Product Management

## Overview

The Product Management page provides a centralized view of all products you've submitted to the Vendor Portal. This interface allows you to view, search, filter, and manage your product submissions throughout their lifecycle—from initial upload through approval and synchronization to Catsy.

Unlike the batch-focused view, the Product Management page gives you a product-centric perspective, making it easy to track individual products, view their detailed information, and understand their current status in the approval workflow.

## Key Concepts

### What is a Product?

A **product** is an individual item you've submitted for approval and eventual synchronization to the Catsy product information management system. Each product has:

- **Unique SKU**: A product identifier that must be unique across your submissions
- **Name**: The product's display name
- **Category**: The hierarchical classification (e.g., Electronics > Audio > Headphones)
- **Status**: Current state in the approval workflow
- **Attributes**: Product characteristics like color, size, material, etc.
- **Pricing**: Optional price and cost information
- **Description**: Detailed product information

### Product Lifecycle

Understanding the product lifecycle helps you track where each product is in the process:

1. **Draft**: Product created but not yet submitted (if manual creation is enabled)
2. **Pending**: Product uploaded and awaiting administrator review
3. **Approved**: Product accepted by administrators and ready for Catsy sync
4. **Rejected**: Product not accepted; requires corrections and resubmission

### Product vs Batch View

**Batch View** (Batch Tracking page):
- Groups products by upload batch
- Focuses on batch-level approval workflow
- Best for tracking recent uploads

**Product View** (Product Management page):
- Shows all products individually
- Focuses on product-level details and status
- Best for searching specific products or reviewing your entire catalog

## Accessing Product Management

### From the Dashboard

1. Click **Products** in the vendor sidebar navigation
2. Or navigate to **My Products** from the main menu

### From the Main Menu

The Products link is always available in your vendor navigation sidebar.

## Product List View

The product list displays all your submitted products with key information at a glance.

### Product List Columns

Each product row shows:

- **Product Name**: The display name of your product
- **SKU**: Unique product identifier
- **Category**: Product category hierarchy (e.g., "Apparel > Men's > Shirts")
- **Status**: Current approval status with color-coded badge
  - 🟢 **Approved** (Green)
  - 🟡 **Pending** (Yellow)
  - 🔴 **Rejected** (Red)
  - 🔵 **Draft** (Blue) - if applicable
- **Date**: When the product was created/uploaded
- **Actions**: Quick action buttons for each product

### Visual Indicators

Products are visually distinguished by status badges:

- **Approved**: Green badge indicating the product is accepted
- **Pending**: Yellow badge indicating awaiting review
- **Rejected**: Red badge indicating corrections needed
- **Draft**: Blue badge indicating not yet submitted

### Search Functionality

At the top of the product list, you'll find a search bar that allows you to quickly find products:

**Search by**:
- Product name (partial matches work)
- SKU (exact or partial matches)

**How to search**:
1. Click in the search box
2. Type your search term
3. Results filter automatically as you type
4. Clear the search box to see all products again

**Search tips**:
- Search is case-insensitive
- Partial matches are supported (searching "shirt" finds "T-Shirt", "Dress Shirt", etc.)
- Search works across both name and SKU fields simultaneously

### Pagination

For vendors with many products, pagination controls appear at the bottom:

- View current page and total pages
- Click **Previous** or **Next** to navigate
- Shows "Showing X to Y of Z products" for context
- Default: 100 products per page

## Product Actions

Each product in the list has action buttons that allow you to interact with it:

### View Product Details

**Icon**: Eye icon (👁️)

**Purpose**: Opens a detailed view of the product with all information

**When to use**: 
- Review complete product information
- Check all attributes and values
- Verify product details before or after submission

**How to use**:
1. Click the eye icon in the Actions column
2. Product detail modal opens
3. Review all product information
4. Click **Close** when finished

### Edit Product

**Icon**: Edit icon (✏️)

**Purpose**: Opens the product editor to modify product information

**When to use**:
- Correct product information
- Update attributes or pricing
- Modify product details before approval

**How to use**:
1. Click the edit icon in the Actions column
2. Product edit modal opens with current values
3. Modify the fields you need to change
4. Click **Save** to update the product

**Important notes**:
- Editing may not be available for all product statuses
- Approved products typically cannot be edited
- Changes to pending products may reset the review process

### Sync to Catsy

**Icon**: Refresh icon (🔄)

**Purpose**: Manually trigger synchronization of an approved product to Catsy

**When available**: Only for products with "Approved" status

**When to use**:
- After a product is approved and you want to ensure it's synced
- To retry a failed sync
- To manually push a product to Catsy

**How to use**:
1. Locate an approved product
2. Click the refresh icon in the Actions column
3. The icon will spin while syncing
4. You'll receive a notification when sync completes
5. Check the product status to confirm successful sync

**Sync status indicators**:
- **Spinning icon**: Sync in progress
- **Success notification**: Product synced successfully
- **Error notification**: Sync failed (check error message)

### Delete Product

**Icon**: Trash icon (🗑️)

**Purpose**: Permanently remove a product from your submissions

**When to use**:
- Remove duplicate products
- Delete products you no longer want to submit
- Clean up draft or rejected products

**How to use**:
1. Click the trash icon in the Actions column
2. Confirmation modal appears
3. Review the product name to ensure you're deleting the correct item
4. Click **Delete** to confirm
5. Product is permanently removed

**Important warnings**:
- Deletion is permanent and cannot be undone
- Approved products may not be deletable
- Consider the impact on your batch records before deleting

## Product Detail View

The product detail modal provides comprehensive information about a specific product.

### Accessing Product Details

Click the eye icon (👁️) in the Actions column for any product to open the detail view.

### Product Information Section

Displays core product metadata:

- **SKU**: Unique product identifier
- **Category**: Full category hierarchy path
- **Status**: Current approval status with color-coded badge
- **Created Date**: When the product was uploaded

### Pricing Section

If your product includes pricing information:

- **Price**: Retail or selling price
- **Cost**: Your cost for the product

Pricing is displayed in currency format (e.g., $29.99).

### Description Section

If your product includes a description:

- Full product description text
- Formatted for readability
- May include multiple paragraphs or detailed information

### Additional Attributes Section

Displays all custom attributes assigned to the product:

- **Attribute Name**: Displayed in readable format (underscores replaced with spaces)
- **Attribute Value**: The value you provided for this product

**Common attributes**:
- Color
- Size
- Material
- Brand
- Weight
- Dimensions
- Style
- Season
- And any custom attributes defined for your category

**Attribute display**:
- Organized in a two-column grid for easy scanning
- Attribute names are uppercase and gray for distinction
- Values are displayed in a larger, darker font for readability

### Closing the Detail View

Click the **Close** button at the bottom of the modal to return to the product list.

## Understanding Product Statuses

### Draft Status

**What it means**:
- Product created but not yet submitted
- Still in preparation phase
- Not visible to administrators

**What you should do**:
- Complete all required fields
- Review product information for accuracy
- Submit the product when ready

**Visual indicator**: Blue badge

### Pending Status

**What it means**:
- Product has been uploaded and submitted
- Awaiting administrator review
- Part of a batch in the review queue

**What to expect**:
- Review typically takes 24-48 hours
- You'll receive a notification when reviewed
- Status will change to Approved or Rejected

**What you should do**:
- Wait patiently for administrator review
- Monitor your notifications for updates
- Ensure you're available to respond to any questions

**Visual indicator**: Yellow badge

### Approved Status

**What it means**:
- Administrators have reviewed and accepted your product
- Product meets all quality standards
- Ready for synchronization to Catsy

**What happens next**:
- Product will be synchronized to Catsy
- Product becomes part of the official catalog
- You can manually trigger sync if needed

**What you should do**:
- Celebrate your successful submission!
- Note what worked well for future products
- Optionally trigger manual sync to Catsy
- Continue with your next products

**Visual indicator**: Green badge

### Rejected Status

**What it means**:
- Administrators reviewed your product and found issues
- Product does not meet quality standards or requirements
- Cannot be synchronized to Catsy in its current state

**What happens next**:
- Review the rejection feedback (available in batch details)
- Identify and correct the issues
- Resubmit as part of a new batch

**What you should do**:
1. Navigate to the batch that contains this product
2. Read the rejection feedback carefully
3. Understand what needs to be corrected
4. Fix the issues in your data
5. Upload a corrected batch with the fixed product
6. Learn from the feedback to improve future submissions

**Visual indicator**: Red badge

**Important**: Rejected products cannot be edited directly in most cases. You'll need to upload a corrected version in a new batch.

## Filtering and Searching Products

### Search by Name or SKU

Use the search bar at the top of the product list:

1. **Click** in the search box
2. **Type** your search term (product name or SKU)
3. **Results filter** automatically as you type
4. **Clear** the search to see all products

**Search examples**:
- Search "shirt" to find all shirt products
- Search "SKU-001" to find a specific SKU
- Search "blue" to find products with "blue" in the name

### Viewing All Products

To see your complete product list:

1. Ensure the search box is empty
2. Navigate through pages using pagination controls
3. All products are displayed in reverse chronological order (newest first)

## Product Management Workflows

### Scenario 1: Checking Product Status

**Situation**: You want to know the status of a specific product.

**Steps**:
1. Navigate to the Products page
2. Use the search bar to find the product by name or SKU
3. Check the status badge in the product row
4. Optionally, click the eye icon to view full details

**Expected outcome**: You can quickly see if the product is pending, approved, or rejected.

### Scenario 2: Viewing Product Details

**Situation**: You need to review all details and attributes for a product.

**Steps**:
1. Locate the product in the product list
2. Click the eye icon (👁️) in the Actions column
3. Review all sections:
   - Product Information
   - Pricing (if applicable)
   - Description (if applicable)
   - Additional Attributes
4. Click **Close** when finished

**Expected outcome**: You have a complete view of all product information and attributes.

### Scenario 3: Syncing an Approved Product

**Situation**: Your product was approved and you want to ensure it's synced to Catsy.

**Steps**:
1. Filter or search for approved products
2. Locate the product you want to sync
3. Click the refresh icon (🔄) in the Actions column
4. Wait for the sync to complete (icon will spin)
5. Check for a success notification
6. Verify the product's sync status

**Expected outcome**: Product is successfully synchronized to Catsy and available in the catalog.

### Scenario 4: Finding Rejected Products

**Situation**: You want to identify all rejected products to understand what needs correction.

**Steps**:
1. Navigate to the Products page
2. Scan the list for red "Rejected" badges
3. Note the SKUs or names of rejected products
4. Navigate to the Batch Tracking page
5. Find the batches containing these products
6. Review the rejection feedback for each batch
7. Prepare corrected data for resubmission

**Expected outcome**: You have a clear list of rejected products and understand what needs to be fixed.

### Scenario 5: Editing Product Information

**Situation**: You need to correct information in a product before it's approved.

**Steps**:
1. Locate the product in the product list
2. Verify the product status allows editing (typically Draft or Pending)
3. Click the edit icon (✏️) in the Actions column
4. Modify the necessary fields in the edit modal
5. Review your changes
6. Click **Save** to update the product
7. Verify the changes were saved successfully

**Expected outcome**: Product information is updated with your corrections.

**Note**: Editing capabilities may be limited based on product status and system configuration.

## Product List Best Practices

### Regular Monitoring

**Check regularly**: Review your product list periodically to track status changes

**Monitor pending products**: Keep track of how long products have been pending
- 0-24 hours: Normal, no action needed
- 24-48 hours: Still normal, continue monitoring
- 48+ hours: Consider following up with your administrator

**Track approval rates**: Monitor the ratio of approved to rejected products to gauge your data quality

### Organizing Your View

**Use search effectively**: Leverage the search function to quickly find specific products

**Track by batch**: Cross-reference with the Batch Tracking page to see products in context

**Note patterns**: If multiple products are rejected, look for common issues to address

### Responding to Status Changes

**Approved products**:
- Verify they appear in your approved list
- Optionally trigger manual sync to Catsy
- Use as examples for future submissions

**Rejected products**:
- Identify all rejected products
- Review batch-level rejection feedback
- Correct issues systematically
- Resubmit in a new batch

**Pending products**:
- Allow adequate time for review
- Don't make changes while pending
- Monitor notifications for updates

### Data Quality Improvement

**Learn from approvals**: Study approved products to understand what works

**Analyze rejections**: Identify patterns in rejected products

**Consistent formatting**: Use the same data format across all products

**Complete information**: Ensure all required fields are filled

**Accurate categorization**: Verify products are in the correct categories

## Common Scenarios

### Scenario: Product Not Appearing in List

**Issue**: Recently uploaded product doesn't show in the product list.

**Solutions**:
- Refresh the page (F5 or Ctrl+R)
- Verify the upload completed successfully
- Check the Batch Tracking page to confirm the batch was created
- Clear your search filter if active
- Wait a few moments and refresh again
- If issue persists after 5 minutes, contact support

### Scenario: Cannot Edit Product

**Issue**: Edit button is disabled or not working.

**Possible reasons**:
- Product status doesn't allow editing (e.g., Approved products)
- Product is currently being reviewed
- System permissions don't allow editing
- Product is part of a locked batch

**Solutions**:
- Check the product status
- If approved, you typically cannot edit (resubmit as new product instead)
- If pending, wait for review to complete
- Contact your administrator if you need to make urgent changes

### Scenario: Sync to Catsy Fails

**Issue**: Manual sync operation fails or shows an error.

**Solutions**:
- Verify the product status is "Approved"
- Check the error message in the notification
- Wait a few minutes and try again
- Verify your internet connection
- Check if Catsy is accessible
- Contact your administrator if sync continues to fail

### Scenario: Product Status Not Updating

**Issue**: Product status seems stuck or not reflecting recent changes.

**Solutions**:
- Refresh the page to get latest data
- Check the Batch Tracking page for batch-level status
- Verify you're viewing the correct product
- Check notifications for status update messages
- Wait a few minutes and refresh again
- Contact administrator if status seems incorrect

### Scenario: Duplicate Products

**Issue**: Same product appears multiple times in the list.

**Explanation**: This can happen if:
- Product was uploaded in multiple batches
- Product was resubmitted after rejection
- SKU was reused (not recommended)

**Solutions**:
- Verify SKUs are truly identical
- Check the dates to identify the most recent version
- Review batch information to understand the context
- Delete older versions if appropriate
- Use unique SKUs for each distinct product

## Tips for Efficient Product Management

### Dashboard Integration

- Use the dashboard for quick statistics
- Navigate to Products page for detailed product-level view
- Cross-reference with Batch Tracking for context

### Search Strategies

- Search by SKU for exact matches
- Search by product name for broader results
- Use partial terms to find related products
- Clear search frequently to avoid missing products

### Status Monitoring

- Regularly check for status changes
- Respond promptly to rejections
- Verify approved products are synced
- Track pending products for timely review

### Organization Tips

- Use consistent naming conventions for products
- Include key identifiers in product names
- Maintain a separate spreadsheet tracking your submissions
- Note batch numbers for each product upload

### Proactive Management

- Review products before they're uploaded
- Ensure data quality at the source
- Learn from rejection patterns
- Maintain consistent attribute values

## Status Indicators Reference

### Product Status Badges

| Status | Color | Icon | Meaning | Your Action |
|--------|-------|------|---------|-------------|
| **Draft** | Blue | Document | Not yet submitted | Complete and submit |
| **Pending** | Yellow | Clock | Awaiting admin review | Wait 24-48 hours, monitor notifications |
| **Approved** | Green | Checkmark | Product accepted | Optionally sync to Catsy |
| **Rejected** | Red | X | Product not accepted | Review feedback, correct issues, resubmit |

### Action Icons

| Icon | Action | Purpose | Availability |
|------|--------|---------|--------------|
| 👁️ | View | See complete product details | All products |
| ✏️ | Edit | Modify product information | Draft/Pending products |
| 🔄 | Sync | Sync to Catsy | Approved products only |
| 🗑️ | Delete | Remove product | Draft/Rejected products |

## Related Topics

### Core Features
- **[Batch Tracking](./batch-tracking.md)** - Track batches and view batch-level status
- **[Product Upload](./product-upload.md)** - Upload products via Excel files
- **[Dashboard](./dashboard.md)** - View product statistics and recent activity

### Before Uploading
- **[Template Builder](./template-builder.md)** - Create Excel templates for uploads
- **[Getting Started](./getting-started.md)** - New vendor quick start guide

### System Features
- **[Notifications](./notifications.md)** - Receive product status notifications
- **[Settings](./settings.md)** - Update profile and preferences

### Common Documentation
- **[Troubleshooting](../common/troubleshooting.md)** - Solutions for product management issues

### Understanding Admin Workflow
- **Admin Product Management** - How admins manage products
- **Admin Batch Management** - How admins review batches

---

**Back to**: [Vendor Documentation](./README.md) | [Home](../README.md)

## Support

If you encounter issues with product management or need assistance:

- Contact your administrator for product-specific questions
- Report technical issues through your support channel
- Refer to the troubleshooting section above for common problems
- Check related documentation for additional guidance

---

**Next Steps**: Learn how to [track your batches](./batch-tracking.md) for batch-level status updates, or explore [notifications](./notifications.md) to stay informed about product status changes.
