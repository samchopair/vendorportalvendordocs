# Vendor Notifications

**Navigation**: [Home](../README.md) > [Vendor Documentation](./README.md) > Notifications

## Overview

The Notification Center is your real-time communication hub for staying informed about your product submissions and batch status updates. As a vendor, you receive instant notifications about batch reviews, upload progress, and important system events, helping you respond quickly to feedback and track your submission workflow.

The notification system uses WebSocket technology to deliver instant updates while you're online, and persists all notifications to ensure you never miss important information even when offline.

## Key Concepts

**Notification Center**: A centralized interface for viewing and managing all your notifications

**Real-Time Delivery**: Notifications appear instantly via WebSocket when you're online

**Persistent Storage**: All notifications are saved to the database for later review

**Notification Types**: Different categories of notifications for various events related to your submissions

**Priority Levels**: Notifications are categorized by importance (low, normal, high, urgent)

**Read Status**: Track which notifications you've reviewed

**Notification Preferences**: Control which notification types you receive and how they're displayed

## Accessing the Notification Center

### Opening the Notification Center

1. Look for the **bell icon** in the top-right corner of the navigation bar
2. The bell displays a **red badge** with the count of unread notifications
3. Click the bell icon to open the notification dropdown panel

### Notification Center Interface

The notification center displays:
- **Header**: "Notifications" title with unread count
- **Notification List**: Scrollable list of recent notifications (up to 20 most recent)
- **Individual Notifications**: Each showing icon, title, message, and timestamp
- **Mark All as Read**: Button to mark all notifications as read at once
- **View All**: Link to see complete notification history (if available)

### Notification Badge

The red badge on the bell icon shows:
- **Number**: Count of unread notifications
- **Visibility**: Only appears when you have unread notifications
- **Updates**: Automatically updates in real-time as new notifications arrive

## Notification Types for Vendors

As a vendor user, you receive the following types of notifications:

### Batch Submitted

**When it occurs**: You successfully submit a new batch of products for review

**What it contains**:
- Batch number (e.g., "BATCH-20251110-001")
- Number of products in the batch
- Confirmation message
- Link to batch detail page

**Example**:
```
Title: Batch Submitted Successfully: BATCH-20251110-001
Message: Your batch with 25 product(s) has been submitted for review. You will be notified when it is reviewed.
Action: Click to view batch details
```

**Priority**: Normal

**What to do**:
- Click the notification to view batch details
- Wait for administrator review (typically 24-48 hours)
- Monitor batch status on your dashboard

### Batch Approved

**When it occurs**: An administrator approves your batch

**What it contains**:
- Batch number
- Number of products approved
- Approver name (if available)
- Link to batch detail page

**Example**:
```
Title: Batch Approved: BATCH-20251110-001
Message: Great news! Your batch BATCH-20251110-001 with 25 product(s) has been approved. Products will be synced.
Action: Click to view batch details
```

**Priority**: Normal

**What to do**:
- Review the approved batch details
- Your products will be automatically synced
- Continue with your next submission

**Celebration**: This is good news! Your products met all requirements and have been accepted.

### Batch Rejected

**When it occurs**: An administrator rejects your batch

**What it contains**:
- Batch number
- Number of products rejected
- Rejection reason and feedback
- Approver name (if available)
- Link to batch detail page

**Example**:
```
Title: Batch Rejected: BATCH-20251110-001
Message: Your batch BATCH-20251110-001 with 25 product(s) has been rejected. Reason: Missing required attributes for several products. Please review the feedback and resubmit.
Action: Click to view batch details and feedback
```

**Priority**: High

**What to do**:
1. Click the notification to view detailed feedback
2. Read the rejection reason carefully
3. Identify which products or fields need correction
4. Download your original file or create a new template
5. Correct the issues based on feedback
6. Upload a new batch with corrected data

**Important**: Rejection feedback is valuable - it helps you improve your data quality for future submissions.

### Upload Progress

**When it occurs**: During an active product upload

**What it contains**:
- Upload progress percentage
- Number of products processed
- Total product count
- Current stage (validating, processing, saving)

**Example**:
```
Type: Upload Progress
Message: Uploading products: 50% complete (25/50 products)
Stage: Validating data...
```

**Priority**: Low

**Note**: This is a transient notification that updates in real-time during uploads and is not persisted to the database.

**What to do**:
- Monitor progress to ensure upload is proceeding
- Wait for upload to complete
- Do not close the browser tab during upload

### Upload Complete

**When it occurs**: Your product upload finishes successfully

**What it contains**:
- Number of products uploaded
- Batch number assigned
- Confirmation message
- Link to batch detail page

**Example (Success)**:
```
Title: Upload Complete
Message: Successfully uploaded 50 product(s) in batch BATCH-20251110-001. Your batch is now pending review.
Action: Click to view batch details
```

**Priority**: Normal

**What to do**:
- Click to view your new batch
- Note the batch number for reference
- Wait for administrator review

### Upload Failed

**When it occurs**: Your product upload encounters an error

**What it contains**:
- Error message
- Number of products that failed
- Reason for failure
- Suggested actions

**Example**:
```
Title: Upload Failed
Message: Failed to upload products. Error: File validation failed - missing required columns. Please check your template and try again.
Action: Click to view upload page
```

**Priority**: High

**What to do**:
1. Read the error message carefully
2. Check your Excel file for issues:
   - Verify you're using the correct template
   - Ensure all required columns are present
   - Check for data format errors
3. Correct the issues
4. Try uploading again

### Validation Errors

**When it occurs**: Your uploaded file contains validation errors

**What it contains**:
- Number of validation errors
- Summary of error types
- Link to detailed error report

**Example**:
```
Title: Validation Errors Found
Message: Your upload contains 5 validation error(s). Common issues: Missing required fields, invalid category IDs. Please review and correct.
Action: Click to view error details
```

**Priority**: High

**What to do**:
1. Click to view detailed error report
2. Review each validation error
3. Correct the issues in your Excel file
4. Re-upload the corrected file

### Product Status Update

**When it occurs**: Individual product status changes (if tracked separately from batch)

**What it contains**:
- Product name or SKU
- Old status
- New status
- Reason for change (if applicable)

**Example**:
```
Title: Product Status Updated
Message: Product "Widget Pro 2000" status changed from Pending to Approved.
Action: Click to view product details
```

**Priority**: Normal

**Note**: This notification type may be disabled by default to reduce notification volume, as batch-level notifications typically provide sufficient information.

## Using the Notification Center

### Viewing Notifications

1. Click the bell icon to open the notification center
2. Scroll through the list of notifications
3. Each notification displays:
   - **Icon**: Visual indicator of notification type
   - **Title**: Brief summary of the event
   - **Message**: Detailed information
   - **Time**: How long ago the notification was created (e.g., "2 hours ago")
   - **Read Status**: Unread notifications have a blue dot or highlighted background

### Reading a Notification

1. Click on any notification in the list
2. The notification is marked as read automatically
3. If the notification has an action URL, you're navigated to the relevant page (batch details, upload page, etc.)
4. The unread count badge decreases by one

### Marking Notifications as Read

**Individual Notification**:
- Click on the notification to mark it as read

**All Notifications**:
1. Click the **Mark All as Read** button at the bottom of the notification center
2. All unread notifications are marked as read
3. The unread count badge disappears

### Notification Timestamps

Notifications display relative timestamps:
- **Just now**: Created within the last minute
- **X minutes ago**: Created within the last hour
- **X hours ago**: Created within the last 24 hours
- **X days ago**: Created more than 24 hours ago
- **X weeks ago**: Created more than 7 days ago

### Notification Actions

Many notifications include action links that navigate you to relevant pages:
- **Batch notifications**: Navigate to batch detail page to view full information
- **Upload notifications**: Navigate to upload page or batch details
- **Error notifications**: Navigate to upload page with error details
- **Product notifications**: Navigate to product detail view

## Notification Preferences

### Accessing Notification Preferences

1. Open the notification center by clicking the bell icon
2. Click the **gear icon** or **Preferences** button in the notification center header
3. The Notification Preferences modal opens

### Configuring Notification Types

Control which types of notifications you receive:

**Available Notification Types**:
- **Batch Submitted**: Confirmation when you submit a batch
- **Batch Approved**: Notification when your batch is approved
- **Batch Rejected**: Notification when your batch is rejected
- **Upload Progress**: Real-time upload progress updates
- **Upload Complete**: Notification when upload finishes
- **Upload Failed**: Notification when upload encounters errors
- **Validation Errors**: Notification about data validation issues
- **Product Status Update**: Individual product status changes

**How to configure**:
1. Open notification preferences
2. Toggle each notification type on or off using the switches
3. Enabled types show a blue switch; disabled types show a gray switch
4. Changes are saved automatically

**Recommended Settings**:
- **Keep enabled**: Batch Approved, Batch Rejected, Upload Complete, Upload Failed, Validation Errors
- **Optional**: Batch Submitted (you already know when you submit)
- **Disable if distracting**: Upload Progress, Product Status Update

### Display Preferences

Control how notifications are displayed:

**Show Toast Notifications**:
- **Enabled**: Notifications appear as toast popups in the corner of the screen
- **Disabled**: Notifications only appear in the notification center
- **Recommendation**: Enable for important notifications like batch approvals and rejections

**Play Sound**:
- **Enabled**: A sound plays when new notifications arrive
- **Disabled**: Notifications arrive silently
- **Recommendation**: Enable if you work in multiple browser tabs or windows

**How to configure**:
1. Open notification preferences
2. Toggle "Show Toast Notifications" on or off
3. Toggle "Play Sound" on or off
4. Changes are saved automatically

### Default Preferences

If you haven't configured preferences, the system uses these defaults:
- **All notification types**: Enabled
- **Show Toast Notifications**: Enabled
- **Play Sound**: Disabled

## Real-Time Notifications

### How Real-Time Delivery Works

The notification system uses WebSocket technology to deliver notifications instantly:

1. **Connection**: When you log in, your browser establishes a WebSocket connection to the server
2. **Online Status**: The server tracks that you're online and ready to receive notifications
3. **Instant Delivery**: When an event occurs (batch reviewed, upload complete, etc.), the server sends the notification immediately to your browser
4. **Persistence**: The notification is also saved to the database for later review

### Online vs Offline Behavior

**When you're online**:
- Notifications appear instantly in the notification center
- Toast notifications pop up (if enabled)
- Sound plays (if enabled)
- Unread count badge updates in real-time
- Upload progress updates in real-time

**When you're offline**:
- Notifications are saved to the database
- When you log back in, you see all notifications you missed
- Unread count reflects all unread notifications
- No real-time updates during offline period

### Multiple Sessions

If you're logged in from multiple devices or browser tabs:
- Notifications are delivered to all active sessions
- Marking a notification as read in one session updates all sessions
- Unread count stays synchronized across all sessions
- Upload progress appears in the tab where you initiated the upload

## Notification Workflow

### Daily Notification Review Routine

Follow this routine to stay on top of your submissions:

1. **Check Unread Count**
   - Look at the bell icon badge when you log in
   - Note how many unread notifications you have

2. **Review New Notifications**
   - Open the notification center
   - Read through unread notifications
   - Prioritize high-priority notifications (rejections, errors)

3. **Take Action**
   - Click on batch rejection notifications to view feedback
   - Review upload completion notifications
   - Address any validation errors or upload failures

4. **Mark as Read**
   - Click "Mark All as Read" after reviewing all notifications
   - Keep your notification center organized

5. **Adjust Preferences**
   - If you're receiving too many notifications, adjust your preferences
   - Disable notification types that aren't helpful

### Responding to Critical Notifications

**High Priority Notifications** (Batch Rejected, Upload Failed, Validation Errors):
1. Read the notification immediately
2. Click to navigate to the relevant page
3. Review detailed feedback or error messages
4. Take corrective action:
   - Fix data issues in your Excel file
   - Correct validation errors
   - Re-upload corrected data
5. Monitor for confirmation of successful resubmission

**Normal Priority Notifications** (Batch Approved, Upload Complete):
1. Review within a few hours
2. Confirm successful completion
3. Continue with your next submission
4. No immediate action required

**Low Priority Notifications** (Upload Progress, Batch Submitted):
1. Review when convenient
2. Use for awareness of system activity
3. No action required

## Tips and Best Practices

### Staying Organized

- **Review notifications daily** to avoid backlog
- **Mark notifications as read** after reviewing them
- **Use action links** to navigate directly to relevant pages
- **Adjust preferences** to reduce notification noise
- **Keep the notification center clean** by regularly marking items as read

### Optimizing Notification Settings

- **Enable critical notifications**: Batch Approved, Batch Rejected, Upload Failed
- **Disable transient notifications**: Upload Progress if you find them distracting
- **Use toast notifications** for important events you don't want to miss
- **Disable sound** if you work in a shared environment or find it distracting

### Managing Notification Volume

If you're receiving too many notifications:
1. Review your notification preferences
2. Disable notification types that aren't helpful (e.g., Batch Submitted, Product Status Update)
3. Consider disabling toast notifications and checking the center periodically
4. Focus on batch-level notifications rather than individual product updates

### Responding to Feedback

When you receive a batch rejection notification:
1. **Don't panic** - rejections are a normal part of the process
2. **Read feedback carefully** - understand what needs to be corrected
3. **Identify patterns** - if you see repeated issues, improve your data preparation process
4. **Ask for help** - contact your administrator if feedback is unclear
5. **Learn and improve** - use feedback to improve future submissions

### Accessibility

- **Keyboard Navigation**: Use Tab to navigate through notifications, Enter to open
- **Screen Reader Support**: All notifications have descriptive labels
- **Visual Indicators**: Unread notifications are clearly marked
- **Color Contrast**: Notification colors meet accessibility standards

## Common Issues

### Notifications Not Appearing

**Symptom**: New notifications don't appear in the notification center

**Possible Causes**:
- WebSocket connection lost
- Browser blocking WebSocket connections
- Notification type disabled in preferences
- Network connectivity issues

**Solutions**:
1. Refresh the page to re-establish WebSocket connection
2. Check browser console for WebSocket errors
3. Verify notification preferences are enabled
4. Check your internet connection
5. Try a different browser
6. Contact your administrator if issue persists

### Unread Count Incorrect

**Symptom**: Unread count badge doesn't match actual unread notifications

**Possible Causes**:
- Synchronization delay
- Multiple sessions with different states
- Browser cache issues

**Solutions**:
1. Refresh the page
2. Click "Mark All as Read" and refresh
3. Clear browser cache and cookies
4. Sign out and sign back in

### Toast Notifications Not Showing

**Symptom**: Toast notifications don't pop up when new notifications arrive

**Possible Causes**:
- Toast notifications disabled in preferences
- Browser notification permissions denied
- Browser blocking popups

**Solutions**:
1. Open notification preferences and enable "Show Toast Notifications"
2. Check browser notification permissions
3. Allow popups for the Vendor Portal domain
4. Refresh the page after changing settings

### Sound Not Playing

**Symptom**: No sound plays when notifications arrive

**Possible Causes**:
- Sound disabled in preferences
- Browser audio muted
- System volume muted

**Solutions**:
1. Open notification preferences and enable "Play Sound"
2. Check browser audio settings
3. Check system volume settings
4. Test with other audio on the website

### Missing Notifications

**Symptom**: Expected notifications didn't arrive

**Possible Causes**:
- Notification type disabled in preferences
- Event didn't trigger notification
- Notification delivery failed

**Solutions**:
1. Check notification preferences to ensure type is enabled
2. Verify the event actually occurred (check batch list, upload history, etc.)
3. Check with your administrator to see if they performed the action
4. Review server logs for notification errors (contact administrator)
5. Refresh the page to sync notifications

### Upload Progress Not Updating

**Symptom**: Upload progress notification stuck or not updating

**Possible Causes**:
- WebSocket connection lost during upload
- Upload stalled or failed
- Browser tab in background (some browsers throttle background tabs)

**Solutions**:
1. Keep the upload tab in the foreground
2. Check your internet connection
3. Refresh the page (upload may need to be restarted)
4. Try uploading again with a smaller batch
5. Contact administrator if issue persists

## Related Topics

### Core Features
- **[Batch Tracking](./batch-tracking.md)** - Tracking batch status triggered by notifications
- **[Product Upload](./product-upload.md)** - Uploading products and receiving progress notifications
- **[Product Management](./product-management.md)** - Viewing products mentioned in notifications
- **[Dashboard](./dashboard.md)** - Dashboard overview with batch statistics

### Getting Started
- **[Getting Started](./getting-started.md)** - New vendor quick start guide
- **[Settings](./settings.md)** - Configure notification preferences
- **[Template Builder](./template-builder.md)** - Create Excel templates

### Common Documentation
- **[Notifications System](../common/notifications-system.md)** - Detailed notification system documentation
- **[Troubleshooting](../common/troubleshooting.md)** - Solutions for notification issues

### Understanding Admin Workflow
- **Admin Notifications** - What notifications admins receive
- **Admin Batch Management** - How admins review batches

---

**Back to**: [Vendor Documentation](./README.md) | [Home](../README.md)

