# Batch Tracking

**Navigation**: [Home](../README.md) > [Vendor Documentation](./README.md) > Batch Tracking

## Overview

Batch tracking allows you to monitor the status of your product submissions from upload through approval. When you upload products via Excel files, they are grouped into batches that go through an administrator review process. The batch tracking interface helps you understand where your products are in the approval workflow and provides detailed information about each submission.

This page covers how to view your batches, understand batch statuses, track the approval process, respond to rejection feedback, and resubmit corrected products.

## Key Concepts

### What is a Batch?

A **batch** is a collection of products uploaded together through a single Excel file. Each batch:

- Has a unique batch number for tracking (e.g., BATCH-20241111-001)
- Contains one or more products from your upload
- Belongs to your vendor organization
- Has a status that changes as it moves through the approval workflow
- Maintains a complete timeline of events from upload to final decision

### Batch Lifecycle

Understanding the batch lifecycle helps you know what to expect after uploading products:

1. **Upload**: You upload an Excel file with products
2. **Validation**: System validates data format and required fields
3. **Batch Creation**: Valid products are grouped into a batch with "Pending" status
4. **Admin Review**: Administrators review your batch and products
5. **Decision**: Batch is either approved or rejected with feedback
6. **Notification**: You receive a notification about the decision
7. **Next Steps**: 
   - **If Approved**: Products are ready for synchronization
   - **If Rejected**: Review feedback, correct issues, and resubmit

### Batch Statuses

Your batches can have one of three statuses:

- **Pending** (Yellow badge): Awaiting administrator review
- **Approved** (Green badge): All products accepted and ready for sync
- **Rejected** (Red badge): Batch not accepted; requires corrections and resubmission

## Accessing Batch Tracking

### From the Dashboard

1. Click **Batches** in the vendor sidebar navigation
2. Or click **View All** in the "My Batches" section of your dashboard
3. Or click on any individual batch in the dashboard to view its details

### From the Main Menu

Navigate to **Batches** from the main vendor menu to see all your batches.

## Batch List View

The batch list displays all your submitted batches with key information at a glance.

### Batch List Columns

Each batch row shows:

- **Batch Number**: Unique identifier for tracking (e.g., BATCH-20241111-001)
- **Status Badge**: Color-coded indicator of current status
  - 🟢 **Approved** (Green)
  - 🟡 **Pending** (Yellow)
  - 🔴 **Rejected** (Red)
- **Filename**: Original Excel filename you uploaded
- **Product Count**: Number of products in the batch
- **Upload Date**: When you submitted the batch (relative time: "2 hours ago", "1 day ago")

### Visual Indicators

Batches are visually distinguished by status:

- **Pending batches**: Light yellow background to highlight batches awaiting review
- **Approved batches**: Green status badge
- **Rejected batches**: Red status badge with alert icon

### Sorting and Filtering

The batch list is automatically sorted by upload date (most recent first), making it easy to find your latest submissions.

### Pagination

For vendors with many batches, pagination controls appear at the bottom:

- View current page and total pages
- Click **Previous** or **Next** to navigate
- Shows "Showing X to Y of Z batches" for context

### Opening a Batch

Click anywhere on a batch row to open the detailed batch view and see complete information.

## Batch Detail View

The batch detail page provides comprehensive information about a specific batch, including all products, timeline, and status updates.

### Batch Information Section

At the top of the page, you'll see key metadata:

- **Batch Number**: Unique identifier for reference
- **Filename**: Original uploaded file name
- **Upload Date**: Full timestamp of when you submitted the batch
- **Product Count**: Total number of products in the batch
- **Status**: Current status with color-coded badge

### Status Information Section

This section shows approval or rejection details:

**For Pending Batches**:
- Status: "Pending"
- Message: "Awaiting administrator review"
- Expected timeline: Typically reviewed within 24-48 hours

**For Approved Batches**:
- Status: "Approved"
- Approval Date: When the administrator approved the batch
- Message: "All products in this batch have been approved"
- Next steps: Products will be synchronized

**For Rejected Batches**:
- Status: "Rejected"
- Rejection Date: When the administrator rejected the batch
- Rejection Reason: Detailed feedback explaining why the batch was rejected
- Next steps: Review feedback, correct issues, and resubmit

### Batch Timeline

The timeline shows a chronological history of all batch events:

- **Batch Created**: Initial upload timestamp with your user information
- **Batch Approved**: Approval timestamp and administrator name (if approved)
- **Batch Rejected**: Rejection timestamp, administrator name, and reason (if rejected)

The timeline helps you:
- Track how long your batch has been in review
- See who made decisions on your batch
- Understand the complete history for reference

### Products Table

Lists all products included in the batch:

- **SKU**: Product identifier
- **Name**: Product name
- **Category**: Product category hierarchy
- **Price**: Product retail price (if provided)
- **Cost**: Product cost (if provided)

You can review all products to verify what was submitted in the batch.

### Batch Actions

**Download Excel Button**:
- Located in the top-right corner
- Downloads the batch data as an Excel file
- Useful for reviewing offline or comparing with your original file
- Filename format: `batch_[BATCH-NUMBER]_[ORIGINAL-FILENAME].xlsx`

## Understanding Batch Statuses

### Pending Status

**What it means**:
- Your batch has been successfully uploaded
- Products passed initial validation
- Batch is in the administrator review queue
- No action required from you at this time

**What to expect**:
- Review typically takes 24-48 hours
- You'll receive a notification when a decision is made
- Check the batch detail page for timeline updates

**What you should do**:
- Wait patiently for administrator review
- Monitor your notifications for updates
- Ensure you're available to respond if administrators have questions
- Continue with other work or prepare your next batch

**Timeline indicators**:
- "Just uploaded": Within the last hour
- "Uploaded 2 hours ago": Still very recent
- "Uploaded 1 day ago": Normal review timeframe
- "Uploaded 3+ days ago": May want to follow up with your administrator

### Approved Status

**What it means**:
- Administrators have reviewed and accepted your batch
- All products in the batch meet quality standards
- Products are approved for synchronization
- Your submission was successful

**What happens next**:
- Products will be synchronized by administrators
- Products become part of the official product catalog
- You can view approved products in the Products page
- Your approval rate statistics improve

**What you should do**:
- Celebrate your successful submission!
- Note what worked well for future uploads
- Maintain the same data quality standards
- Continue with your next batch if you have more products

**No action required**: Approved batches are complete and need no further attention from you.

### Rejected Status

**What it means**:
- Administrators reviewed your batch and found issues
- Products do not meet quality standards or requirements
- Batch cannot be synchronized in its current state
- You need to correct the issues and resubmit

**What happens next**:
- Review the rejection feedback carefully
- Identify and correct the issues
- Prepare a new batch with corrected data
- Upload the corrected batch as a new submission

**What you should do**:
1. Read the rejection reason thoroughly
2. Understand what needs to be corrected
3. Fix the identified issues in your data
4. Resubmit as a new batch
5. Learn from the feedback to improve future submissions

**Important**: Rejected batches cannot be edited or resubmitted directly. You must create a new batch with corrected data.

## Understanding Rejection Feedback

When a batch is rejected, administrators provide detailed feedback explaining what needs to be corrected.

### Reading Rejection Feedback

The rejection reason appears in the Status Information section of the batch detail page. It typically includes:

- **Specific issues**: What problems were found
- **Affected products**: Which SKUs or products have issues (if applicable)
- **Required corrections**: What needs to be fixed
- **Guidance**: How to correct the issues

### Common Rejection Reasons

**Missing Required Attributes**

Example feedback:
```
Missing required attributes: Color and Size are required for all products 
in the Apparel category. Please add these attributes and resubmit.
```

**What to do**:
1. Identify which attributes are missing
2. Download a new template that includes those attributes
3. Add the missing attribute values to your products
4. Upload the corrected batch

**Invalid Category Assignments**

Example feedback:
```
Invalid category assignments - products should be in Electronics > Accessories, 
not Electronics > Audio. Please correct the categories and resubmit.
```

**What to do**:
1. Note the correct category path
2. Update your Excel file with the correct categories
3. Use the category dropdown in the template to ensure accuracy
4. Resubmit with corrected categories

**Pricing Errors**

Example feedback:
```
Pricing errors: Cost exceeds price for SKUs 12345, 12346, 12347. 
Please verify pricing and correct.
```

**What to do**:
1. Review the specified SKUs
2. Verify that price is greater than cost
3. Correct any pricing errors
4. Double-check all other products for similar issues
5. Resubmit with corrected pricing

**Duplicate SKUs**

Example feedback:
```
Duplicate SKUs found: SKU-001 appears 3 times in the batch. 
Each SKU must be unique. Please correct and resubmit.
```

**What to do**:
1. Find all instances of the duplicate SKU
2. Assign unique SKUs to each product
3. Verify no other duplicates exist
4. Resubmit with unique SKUs

**Data Quality Issues**

Example feedback:
```
Multiple data quality issues: Missing descriptions for 15 products, 
invalid price formats for SKUs 100-105, and incomplete attribute 
values. Please review and correct all data quality issues.
```

**What to do**:
1. Address each issue mentioned
2. Review all products for similar problems
3. Improve overall data quality
4. Consider uploading smaller test batches first
5. Resubmit when all issues are resolved

### Interpreting Feedback

**Be thorough**: Address all issues mentioned, not just the first one

**Look for patterns**: If multiple products have the same issue, fix the root cause

**Ask for clarification**: If feedback is unclear, contact your administrator

**Learn from feedback**: Use rejection reasons to improve future submissions

## Resubmitting Corrected Products

After receiving rejection feedback, follow these steps to correct and resubmit your products.

### Step-by-Step: Resubmission Process

#### 1. Review Rejection Feedback

- Open the rejected batch detail page
- Read the rejection reason carefully
- Note all specific issues mentioned
- Identify which products or fields need correction

#### 2. Download the Batch (Optional)

- Click **Download Excel** on the batch detail page
- This gives you the exact data that was rejected
- Use this as a reference for corrections
- Compare with your original file to identify issues

#### 3. Correct the Issues

**Option A: Fix Your Original File**
- Open your original Excel file
- Make the required corrections based on feedback
- Verify all issues are addressed
- Save the corrected file

**Option B: Start with a New Template**
- Navigate to the Template Builder
- Build a new template with the correct categories and attributes
- Copy your product data to the new template
- Make corrections as you transfer the data
- Save the new file

#### 4. Validate Your Corrections

Before uploading, double-check:
- All issues from rejection feedback are fixed
- No new errors were introduced
- Required fields are complete
- Categories are from the dropdown
- SKUs are unique
- Prices and costs are formatted correctly
- Attributes are filled in properly

#### 5. Upload the Corrected Batch

- Navigate to the Upload page
- Upload your corrected Excel file
- Review the preview carefully
- Verify all products show as valid (green checkmarks)
- Confirm and create the new batch

#### 6. Monitor the New Batch

- Note the new batch number
- The new batch will have "Pending" status
- Monitor notifications for the review decision
- The new batch is independent of the rejected batch

### Important Notes About Resubmission

**New Batch Creation**: Resubmissions create a new batch with a new batch number. The rejected batch remains in your history for reference.

**No Direct Editing**: You cannot edit or reopen a rejected batch. You must upload a new batch.

**All Products**: Even if only some products had issues, you typically need to resubmit all products in a new batch.

**Learning Opportunity**: Use rejection feedback to improve your data preparation process for future uploads.

**Faster Approval**: Batches that address feedback thoroughly are often approved more quickly on resubmission.

## Downloading Batch Data

You can download any batch as an Excel file for offline review, record-keeping, or comparison.

### How to Download

1. **Open Batch Detail Page**
   - Navigate to the batch you want to download
   - Click on the batch from the batch list

2. **Click Download Button**
   - Click **Download Excel** in the top-right corner
   - The button shows a download icon

3. **Wait for Generation**
   - The button shows "Downloading..." with a spinner
   - The system generates the Excel file (usually takes a few seconds)

4. **File Downloads**
   - The Excel file downloads to your device
   - Filename format: `batch_[BATCH-NUMBER]_[ORIGINAL-FILENAME].xlsx`
   - Success notification appears

### Downloaded File Contents

The Excel file includes:

- **All products** from the batch
- **Standard columns**: SKU, Name, Category, Description, Price, Cost
- **Attribute columns**: All product attributes with their values
- **Formatted headers**: Bold headers with gray background for readability
- **Auto-sized columns**: Columns adjusted to fit content

### Use Cases for Downloading

**Offline Review**:
- Review batch details without internet access
- Work on corrections offline
- Share with team members for review

**Comparison**:
- Compare downloaded batch with your original file
- Identify what data was actually submitted
- Verify data integrity

**Correction Reference**:
- Use as a starting point for fixing rejected batches
- See exactly what was submitted
- Ensure corrections address the right issues

**Record Keeping**:
- Archive batch data for your records
- Maintain submission history
- Document what was submitted and when

**Analysis**:
- Analyze submission patterns
- Review product data in Excel
- Use Excel features (sorting, filtering, formulas) for analysis

## Batch Tracking Best Practices

### Regular Monitoring

**Check Daily**: Review your batch list at least once per day during active submission periods

**Monitor Pending Batches**: Keep track of how long batches have been pending
- 0-24 hours: Normal, no action needed
- 24-48 hours: Still normal, continue monitoring
- 48+ hours: Consider following up with your administrator

**Watch Notifications**: Enable notifications to receive immediate updates about batch decisions

### Responding to Decisions

**Approved Batches**:
- Note what worked well
- Apply the same standards to future uploads
- Maintain consistent data quality

**Rejected Batches**:
- Respond promptly to rejection feedback
- Correct issues within 1-2 business days
- Resubmit as soon as corrections are complete
- Learn from feedback to prevent similar issues

### Improving Approval Rates

**Quality Over Speed**: Take time to ensure data quality before uploading

**Test Small Batches**: Upload 10-20 products first to validate your format

**Use Templates Correctly**: Always use the template builder and don't modify template structure

**Validate Before Upload**: Review your data in Excel before uploading

**Learn from Rejections**: Analyze rejection patterns and improve your process

**Consistent Formatting**: Use the same data format across all uploads

### Record Keeping

**Track Batch Numbers**: Keep a log of batch numbers and upload dates

**Save Original Files**: Maintain copies of all uploaded Excel files

**Document Feedback**: Keep notes on rejection feedback and how you addressed it

**Monitor Trends**: Track your approval rate over time

## Common Scenarios

### Scenario 1: Tracking a New Upload

**Situation**: You just uploaded a batch and want to track its progress.

**Steps**:
1. Note the batch number from the success screen
2. Navigate to the Batches page
3. Find your batch at the top of the list (most recent)
4. Verify status shows "Pending"
5. Check back in 24-48 hours for updates
6. Monitor notifications for decision alerts

**Expected outcome**: Batch appears with "Pending" status and is reviewed within 24-48 hours.

### Scenario 2: Responding to Rejection

**Situation**: You received a notification that your batch was rejected.

**Steps**:
1. Click the notification or navigate to Batches
2. Open the rejected batch
3. Read the rejection reason carefully
4. Download the batch Excel file for reference
5. Identify all issues mentioned in the feedback
6. Open your original file or create a new template
7. Correct all identified issues
8. Validate your corrections
9. Upload the corrected batch
10. Monitor the new batch for approval

**Expected outcome**: New batch is approved after addressing all feedback.

### Scenario 3: Batch Pending for Multiple Days

**Situation**: Your batch has been pending for 3+ days without a decision.

**Steps**:
1. Open the batch detail page
2. Verify the status is still "Pending"
3. Check the timeline for any updates
4. Review your notifications for any administrator questions
5. Contact your administrator to inquire about the status
6. Provide the batch number for reference

**Expected outcome**: Administrator provides an update or reviews the batch promptly.

### Scenario 4: Comparing Rejected Batch with Original

**Situation**: You want to understand what data was actually submitted in a rejected batch.

**Steps**:
1. Open the rejected batch detail page
2. Click **Download Excel** to get the submitted data
3. Open your original Excel file
4. Compare the two files side-by-side
5. Identify any differences or issues
6. Use the rejection feedback to guide your comparison
7. Correct issues in your original file
8. Resubmit the corrected batch

**Expected outcome**: You identify the exact issues and can correct them accurately.

### Scenario 5: Multiple Batches in Review

**Situation**: You have several batches pending review simultaneously.

**Steps**:
1. Navigate to the Batches page
2. Review all pending batches (yellow background)
3. Note the upload date for each
4. Prioritize monitoring based on upload date (oldest first)
5. Check notifications regularly for updates
6. Respond to any decisions promptly

**Expected outcome**: All batches are reviewed in order, and you respond to each decision appropriately.

## Troubleshooting

### Batch Not Appearing in List

**Issue**: Recently uploaded batch doesn't show in the batch list.

**Solutions**:
- Refresh the page (F5 or Ctrl+R)
- Verify the upload completed successfully (check for success message)
- Check your notifications for upload errors
- Navigate away and back to the Batches page
- If issue persists after 5 minutes, contact support

### Batch Detail Page Not Loading

**Issue**: Clicking a batch shows an error or loading spinner indefinitely.

**Solutions**:
- Refresh the page
- Check your internet connection
- Try opening a different batch to verify the page works
- Clear browser cache and cookies
- Try a different browser
- Contact support if issue persists

### Cannot Download Batch

**Issue**: Download Excel button doesn't work or download fails.

**Solutions**:
- Check browser's download settings and permissions
- Ensure pop-ups are not blocked for the site
- Verify you have sufficient disk space
- Try again - click the button once and wait
- Try a different browser
- Check browser console for error messages

### Status Not Updating

**Issue**: Batch status seems stuck or not reflecting recent changes.

**Solutions**:
- Refresh the page to get latest data
- Check notifications for status update messages
- Verify you're viewing the correct batch
- Wait a few minutes and refresh again
- Contact administrator if status seems incorrect

### Missing Rejection Feedback

**Issue**: Batch shows as rejected but no rejection reason is displayed.

**Solutions**:
- Refresh the page
- Check if feedback appears in the Status Information section
- Look for feedback in the timeline
- Check your notifications for rejection details
- Contact the administrator who rejected the batch for clarification

### Duplicate Batch Numbers

**Issue**: Two batches seem to have the same or similar batch numbers.

**Solutions**:
- Verify the complete batch number (including date and sequence)
- Batch numbers are unique - similar numbers may differ in date or sequence
- Check the upload date to distinguish between batches
- Use filename and product count as additional identifiers

## Tips for Efficient Batch Tracking

### Dashboard Integration

- Use the dashboard "My Batches" widget for quick status checks
- The dashboard shows your most recent batches
- Pending batch count is highlighted for visibility
- Click through to batch details directly from the dashboard

### Notification Strategy

- Enable browser notifications for real-time updates
- Check the notification center (bell icon) regularly
- Notifications alert you immediately when batches are reviewed
- Don't rely solely on email - use in-app notifications

### Batch Organization

- Use descriptive filenames when uploading (e.g., "Apparel_Winter_2024.xlsx")
- Upload related products together in logical batches
- Keep batch sizes manageable (100-500 products per batch)
- Track batch numbers in your own records for reference

### Proactive Communication

- If you have urgent batches, communicate with your administrator
- Provide context in your filename or through other channels
- Be responsive to administrator questions or feedback
- Build a good working relationship with your reviewers

## Status Indicators Reference

### Batch Status Badges

| Status | Color | Icon | Meaning | Your Action |
|--------|-------|------|---------|-------------|
| **Pending** | Yellow | Clock | Awaiting admin review | Wait 24-48 hours, monitor notifications |
| **Approved** | Green | Checkmark | Batch accepted | No action needed, products will sync |
| **Rejected** | Red | X | Batch not accepted | Review feedback, correct issues, resubmit |

### Timeline Event Types

| Event | Description | Information Shown |
|-------|-------------|-------------------|
| **Batch Created** | Initial upload | Upload timestamp, your user name |
| **Batch Approved** | Admin approval | Approval timestamp, admin name |
| **Batch Rejected** | Admin rejection | Rejection timestamp, admin name, reason |

### Time Indicators

The batch list uses relative time indicators:

- **"Just now"**: Within the last minute
- **"X minutes ago"**: Within the last hour
- **"X hours ago"**: Within the last 24 hours
- **"X days ago"**: More than 24 hours ago
- **"X weeks ago"**: More than 7 days ago

This helps you quickly assess the recency of uploads and how long batches have been pending.

## Related Topics

### Core Features
- **[Product Upload](./product-upload.md)** - Upload products and create batches
- **[Product Management](./product-management.md)** - View and manage individual products
- **[Dashboard](./dashboard.md)** - View batch statistics and recent batches

### Before Uploading
- **[Template Builder](./template-builder.md)** - Create Excel templates for uploads
- **[Getting Started](./getting-started.md)** - New vendor quick start guide

### System Features
- **[Notifications](./notifications.md)** - Receive batch status notifications
- **[Settings](./settings.md)** - Update profile and preferences

### Common Documentation
- **[Troubleshooting](../common/troubleshooting.md)** - Solutions for batch tracking issues

### Understanding Admin Workflow
- **Admin Batch Management** - How admins review and approve batches
- **Admin Product Management** - What happens after approval

---

**Back to**: [Vendor Documentation](./README.md) | [Home](../README.md)

## Support

If you encounter issues with batch tracking or need assistance:

- Contact your administrator for batch-specific questions
- Report technical issues through your support channel
- Refer to the troubleshooting section above for common problems
- Check related documentation for additional guidance

---

**Next Steps**: Learn how to [manage your products](./product-management.md) after batch approval, or explore [notification settings](./notifications.md) to stay informed about batch updates.
