# Notifications System

**Navigation**: [Home](../README.md) > [Common Documentation](../README.md#common-topics) > Notifications System

## Overview

The Vendor Portal features a comprehensive real-time notification system that keeps you informed about important events and updates. Notifications are delivered instantly via WebSocket connections and are also persisted in the database so you never miss important information, even when offline.

## Key Concepts

### Real-Time Delivery

The notification system uses WebSocket technology to deliver notifications instantly:
- **Instant Updates**: Notifications appear immediately when events occur
- **No Page Refresh**: Receive notifications without reloading the page
- **Multiple Sessions**: Notifications delivered to all your active browser tabs/windows
- **Automatic Reconnection**: System automatically reconnects if connection is lost

### Notification Persistence

All notifications (except progress updates) are saved to the database:
- **Offline Access**: View notifications received while you were offline
- **History**: Access your complete notification history
- **Read Status**: Track which notifications you've read
- **Permanent Record**: Notifications remain available until you delete them

### Notification Types

Different types of notifications inform you about various events:

**For Admin Users:**
- **Batch Submitted**: New batch submitted by vendor for review
- **Upload Complete**: Product upload finished
- **Sync Complete**: Category or product sync finished
- **Sync Error**: Sync operation encountered errors
- **System**: Important system announcements

**For Vendor Users:**
- **Batch Approved**: Your batch has been approved
- **Batch Rejected**: Your batch has been rejected with feedback
- **Upload Progress**: Real-time upload progress updates
- **Upload Complete**: Your upload finished
- **System**: Important system announcements

**For All Users:**
- **Info**: General information messages
- **Warning**: Important warnings requiring attention
- **Error**: Error messages requiring action

### Notification Priority

Notifications have different priority levels:
- **Low**: Informational updates, can be reviewed later
- **Normal**: Standard notifications about routine events
- **High**: Important notifications requiring attention (e.g., batch rejections)
- **Urgent**: Critical notifications requiring immediate action

## Notification Center

### Accessing the Notification Center

The notification center is accessible from any page in the application:

1. Look for the bell icon in the top-right corner of the header
2. The bell icon shows a badge with your unread notification count
3. Click the bell icon to open the notification center popover

### Notification Center Interface

The notification center displays:

**Header Section:**
- Title: "Notifications"
- Unread count: Shows how many unread notifications you have
- "Mark all read" button: Quickly mark all notifications as read

**Filter Section:**
- **All/Unread Tabs**: Toggle between viewing all notifications or only unread ones
- **Type Filter**: Filter notifications by type (batch, upload, sync, etc.)

**Notification List:**
- Notifications displayed in reverse chronological order (newest first)
- Visual distinction for unread notifications (bold text, colored indicator)
- Each notification shows:
  - Icon representing the notification type
  - Title and message
  - Timestamp (relative time like "2 minutes ago")
  - Action button or link (if applicable)

**Empty State:**
- Displays when you have no notifications
- Different messages for "all" vs "unread" filters

### Notification Badge

The notification badge on the bell icon:
- Shows the count of unread notifications
- Updates in real-time as new notifications arrive
- Disappears when all notifications are read
- Maximum display is typically "99+" for large numbers

### Interacting with Notifications

**Viewing a Notification:**
1. Click on any notification in the list
2. The notification is automatically marked as read
3. If the notification has an action URL, you'll be navigated to the relevant page

**Marking as Read:**
- Click on a notification to mark it as read
- Use "Mark all read" button to mark all notifications as read at once
- Read notifications have a lighter appearance

**Filtering Notifications:**
1. Use the "All" / "Unread" tabs to filter by read status
2. Use the type dropdown to filter by notification type
3. Filters can be combined for precise results

**Loading More:**
- Scroll to the bottom of the notification list
- Click "Load more" button to fetch older notifications
- Pagination loads 20 notifications at a time

## Notification Types in Detail

### Batch Notifications

**Batch Submitted** (Admin Only)
- **When**: Vendor submits a new batch for review
- **Contains**: Batch number, vendor name, organization, product count
- **Action**: Click to view batch details and review
- **Priority**: Normal

**Batch Approved** (Vendor Only)
- **When**: Admin approves your batch
- **Contains**: Batch number, product count, approver name
- **Action**: Click to view approved batch details
- **Priority**: Normal

**Batch Rejected** (Vendor Only)
- **When**: Admin rejects your batch
- **Contains**: Batch number, product count, approver name, rejection reason
- **Action**: Click to view batch and address issues
- **Priority**: High

### Upload Notifications

**Upload Progress** (Real-Time, Not Persisted)
- **When**: Products are being uploaded
- **Contains**: Progress percentage, current count, total count
- **Display**: Progress bar with percentage
- **Updates**: Real-time updates every few seconds
- **Note**: Not saved to database, only visible while online

**Upload Complete**
- **When**: Product upload finishes
- **Contains**: Success count, failure count, total count, error summary
- **Action**: Click to view upload history details
- **Priority**: Normal (or High if all uploads failed)

### Sync Notifications

**Sync Started** (Real-Time, Not Persisted)
- **When**: Category or product sync begins
- **Contains**: Sync type (products, categories, attributes)
- **Display**: Toast notification
- **Note**: Not saved to database

**Sync Progress** (Real-Time, Not Persisted)
- **When**: Sync operation is in progress
- **Contains**: Progress percentage, current count, total count
- **Display**: Progress indicator
- **Updates**: Real-time updates
- **Note**: Not saved to database

**Sync Complete**
- **When**: Sync operation finishes successfully
- **Contains**: Sync type, item count, duration
- **Action**: Click to view synced items
- **Priority**: Normal

**Sync Error**
- **When**: Sync operation encounters errors
- **Contains**: Sync type, error message, failed count
- **Action**: Click to view error details and retry
- **Priority**: High

### System Notifications

**System Announcements**
- **When**: Administrators send system-wide announcements
- **Contains**: Announcement title and message
- **Priority**: Varies (Normal to Urgent)
- **Examples**: Maintenance windows, new features, policy changes

**Info Messages**
- **When**: General information needs to be communicated
- **Contains**: Informational message
- **Priority**: Low to Normal

**Warnings**
- **When**: Important warnings requiring attention
- **Contains**: Warning message and recommended action
- **Priority**: Normal to High

**Errors**
- **When**: Errors occur that require user action
- **Contains**: Error message and resolution steps
- **Priority**: High

## Notification Preferences

### Accessing Preferences

To configure your notification preferences:

1. Navigate to Settings from the main menu
2. Find the "Notification Preferences" section
3. Adjust your preferences as needed
4. Click "Save preferences" to apply changes

### Display Settings

**Show Toast Notifications**
- **Enabled**: Notifications appear as toast popups in the corner
- **Disabled**: Notifications only appear in the notification center
- **Default**: Enabled
- **Recommendation**: Keep enabled for important updates

**Play Notification Sounds**
- **Enabled**: Play a sound when notifications arrive
- **Disabled**: Silent notifications
- **Default**: Disabled
- **Recommendation**: Enable if you want audio alerts

### Notification Type Preferences

You can enable or disable specific notification types:

**Enabled Types:**
- Notifications of this type will be delivered and displayed
- Saved to database and shown in notification center
- Toast notifications shown (if enabled)

**Disabled Types:**
- Notifications of this type will not be created or delivered
- You won't see them in the notification center
- No toast notifications or sounds

**Default Enabled Types:**
- Batch Submitted
- Batch Approved
- Batch Rejected
- Upload Complete
- Sync Complete
- Sync Error
- System Notifications
- Error Messages

**Typically Disabled by Default:**
- Upload Progress (transient, real-time only)
- Sync Progress (transient, real-time only)
- Info Messages (can be noisy)
- Warnings (unless critical)

### Saving Preferences

1. Make your desired changes to preferences
2. The "Save preferences" button becomes enabled when changes are detected
3. Click "Save preferences" to apply
4. A success message confirms your preferences were saved
5. New preferences take effect immediately

### Resetting Preferences

To restore default notification settings:

1. Click the "Reset to defaults" button
2. Confirm the action
3. All preferences return to system defaults
4. Changes take effect immediately

## Real-Time WebSocket Connection

### How It Works

The notification system uses WebSocket technology for real-time communication:

1. **Connection**: When you sign in, your browser establishes a WebSocket connection
2. **Authentication**: Connection is authenticated using your JWT token
3. **Session Tracking**: Server tracks all your active sessions (browser tabs)
4. **Event Delivery**: When events occur, notifications are sent instantly to all your sessions
5. **Persistence**: Notifications are saved to database before delivery

### Connection Status

The WebSocket connection can be in different states:

**Connected**
- Active connection to the server
- Receiving real-time notifications
- Green indicator (if shown in UI)

**Connecting**
- Attempting to establish connection
- May occur on initial page load or after disconnection
- Yellow indicator (if shown in UI)

**Disconnected**
- No active connection to server
- Not receiving real-time notifications
- Red indicator (if shown in UI)
- System will automatically attempt to reconnect

### Automatic Reconnection

If your WebSocket connection is lost:

1. **Detection**: System detects the disconnection
2. **Retry**: Automatically attempts to reconnect
3. **Exponential Backoff**: Waits progressively longer between retry attempts
4. **Success**: Once reconnected, you'll receive any missed notifications
5. **Persistence**: All notifications are saved, so nothing is lost

**Reconnection Schedule:**
- 1st attempt: Immediate
- 2nd attempt: After 1 second
- 3rd attempt: After 2 seconds
- 4th attempt: After 4 seconds
- 5th attempt: After 8 seconds
- Maximum delay: 30 seconds between attempts

### Multiple Sessions

If you have the Vendor Portal open in multiple browser tabs or windows:
- Each tab maintains its own WebSocket connection
- Notifications are delivered to all active tabs
- Marking a notification as read in one tab updates all tabs
- Closing a tab disconnects only that session

### Offline Behavior

When you're offline or disconnected:
- **Notifications Still Created**: Server creates and saves notifications
- **No Real-Time Delivery**: You won't receive instant notifications
- **Available on Reconnect**: When you reconnect, notifications are available in the notification center
- **No Data Loss**: All notifications are persisted in the database

## Toast Notifications

### What Are Toast Notifications?

Toast notifications are small popup messages that appear temporarily in the corner of your screen to alert you of new notifications without interrupting your work.

### Toast Appearance

Toast notifications typically:
- Appear in the top-right or bottom-right corner
- Display for 3-5 seconds before auto-dismissing
- Show the notification icon, title, and brief message
- Can be manually dismissed by clicking the X button
- Stack vertically if multiple notifications arrive

### Toast Behavior

**Auto-Dismiss:**
- Normal priority: 4 seconds
- High priority: 6 seconds
- Urgent priority: 8 seconds or manual dismiss only

**Click Actions:**
- Click the toast to navigate to the related page
- Toast is marked as read when clicked
- Toast disappears after click

**Multiple Toasts:**
- Multiple toasts stack vertically
- Oldest toasts auto-dismiss first
- Maximum of 3-5 toasts shown at once

### Disabling Toasts

If you find toast notifications distracting:
1. Go to Settings > Notification Preferences
2. Toggle off "Show toast notifications"
3. Save preferences
4. Notifications will only appear in the notification center

## Notification History

### Viewing History

To view your complete notification history:

1. Open the notification center
2. Switch to "All" tab to see all notifications
3. Scroll down to load older notifications
4. Use filters to find specific notifications

### History Retention

Notification history is retained:
- **Indefinitely**: Notifications are not automatically deleted
- **User Control**: You can manually delete notifications (if feature available)
- **Database Storage**: All notifications stored in database
- **Performance**: Pagination ensures fast loading even with many notifications

### Searching History

To find specific notifications:
1. Use the type filter to narrow by notification type
2. Use the unread filter to find unread notifications
3. Scroll through chronological list
4. Look for specific batch numbers, dates, or keywords in titles

## Troubleshooting

### Not Receiving Notifications

**Problem**: No notifications appearing
- **Check**: Notification preferences - ensure types are enabled
- **Check**: WebSocket connection status
- **Check**: Browser console for connection errors
- **Solution**: Refresh page, check network connection

**Problem**: Toast notifications not showing
- **Check**: Toast notifications enabled in preferences
- **Check**: Browser notification permissions
- **Solution**: Enable in preferences, allow browser notifications

**Problem**: Delayed notifications
- **Check**: WebSocket connection status
- **Check**: Network latency
- **Solution**: Refresh page to reconnect, check internet connection

### Connection Issues

**Problem**: Frequent disconnections
- **Cause**: Network instability, firewall, proxy
- **Solution**: Check network connection, contact IT if behind corporate firewall

**Problem**: Cannot connect to WebSocket
- **Cause**: Firewall blocking WebSocket, invalid token
- **Solution**: Check firewall settings, try signing out and back in

**Problem**: "Connection timeout" errors
- **Cause**: Server unreachable, network issues
- **Solution**: Wait for automatic reconnection, refresh page if persists

### Notification Center Issues

**Problem**: Notification center not opening
- **Cause**: JavaScript error, browser compatibility
- **Solution**: Refresh page, try different browser, clear cache

**Problem**: Notifications not marking as read
- **Cause**: API error, network issue
- **Solution**: Try again, refresh page

**Problem**: Old notifications not loading
- **Cause**: API error, database issue
- **Solution**: Refresh page, contact support if persists

## Best Practices

### Managing Notifications

1. **Review Regularly**: Check notification center daily
2. **Mark as Read**: Keep your notification list organized
3. **Use Filters**: Find specific notifications quickly
4. **Configure Preferences**: Disable notification types you don't need
5. **Act Promptly**: Address high-priority notifications quickly

### Staying Informed

1. **Enable Important Types**: Keep batch and error notifications enabled
2. **Use Toast Notifications**: Enable for immediate awareness
3. **Check When Offline**: Review notifications after being offline
4. **Monitor Badge**: Keep an eye on the notification badge count

### Performance Tips

1. **Mark Old Notifications as Read**: Reduces unread count
2. **Use Filters**: Faster than scrolling through all notifications
3. **Close Unused Tabs**: Reduces WebSocket connections
4. **Refresh Periodically**: Clears memory and reconnects

## Related Topics

### Admin Documentation
- **Admin Notifications** - Admin-specific notification types and preferences
- **Admin Dashboard** - Dashboard with notification integration
- **Admin Batch Management** - Batch notifications
- **Admin Settings** - Configure notification preferences

### Vendor Documentation
- **[Vendor Notifications](../vendor/notifications.md)** - Vendor-specific notification types and preferences
- **[Vendor Dashboard](../vendor/dashboard.md)** - Dashboard with notification integration
- **[Vendor Batch Tracking](../vendor/batch-tracking.md)** - Batch status notifications
- **[Vendor Settings](../vendor/settings.md)** - Configure notification preferences

### Common Documentation
- **[Authentication](./authentication.md)** - Session and token management
- **[Troubleshooting](./troubleshooting.md)** - Solutions for notification issues

---

**Back to**: [Home](../README.md)

## Technical Details

### WebSocket Configuration

- **Protocol**: Socket.IO over WebSocket
- **Path**: `/socket.io/`
- **Authentication**: JWT token in connection handshake
- **Ping Interval**: 25 seconds
- **Ping Timeout**: 60 seconds
- **Reconnection**: Automatic with exponential backoff

### Notification Data Structure

Each notification contains:
- **ID**: Unique notification identifier
- **Type**: Notification type (batch_submitted, upload_complete, etc.)
- **Title**: Short notification title
- **Message**: Detailed notification message
- **Meta**: Additional metadata (batch_id, product_count, etc.)
- **Action URL**: Optional URL to navigate to
- **Priority**: Priority level (low, normal, high, urgent)
- **Read**: Read status (true/false)
- **Created At**: Timestamp when notification was created

### API Endpoints

The notification system uses these API endpoints:
- `GET /api/notifications` - List notifications with pagination
- `GET /api/notifications/{id}` - Get specific notification
- `PUT /api/notifications/{id}/read` - Mark notification as read
- `PUT /api/notifications/mark-all-read` - Mark all as read
- `GET /api/notification-preferences` - Get user preferences
- `PUT /api/notification-preferences` - Update preferences
- `POST /api/notification-preferences/reset` - Reset to defaults

## Support

If you experience issues with the notification system:
- Check this documentation for troubleshooting steps
- Verify your notification preferences are configured correctly
- Check your network connection and firewall settings
- Contact your system administrator
- Email support with details of the issue including:
  - Browser and version
  - Error messages from browser console
  - Steps to reproduce the issue
  - Screenshots if applicable
