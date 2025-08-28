# User Management UI — Specification

## Overview
The User Management interface provides administrators with the ability to view, create, and manage user accounts within the system. The interface is divided into two main sections with a user list view on the left and a new user creation form on the right.

## Page Layout

### Two-Column Layout
- **Left Section**: User list and management controls
- **Right Section**: New user creation form

## Left Section: User List and Controls

### Header Controls
1. **"New User" Button**
   - **Style**: Blue button with white text
   - **Position**: Top-left of the left section
   - **Behavior**: Clicking this button should focus the right section form

2. **"Hide Disabled User" Checkbox**
   - **Style**: Standard checkbox with label
   - **Position**: Top-right of the left section, aligned with the "New User" button
   - **Default State**: Checked
   - **Behavior**: When checked, filters out users where "Enabled" = false from the table

### User Data Table

#### Table Structure
- **Header Row**: Blue background with white text
- **Data Rows**: Alternating white and light blue backgrounds for better readability
- **Sortable Columns**: All columns should be sortable with visual indicators

#### Column Specifications

1. **ID Column**
   - **Header**: "ID" with upward arrow and filter icon
   - **Data Type**: Integer
   - **Sorting**: Ascending/Descending toggle
   - **Filtering**: Text input filter for exact or partial matches

2. **User Name Column**
   - **Header**: "User Name" with up/down arrow and filter icon
   - **Data Type**: String
   - **Sorting**: Alphabetical (A-Z, Z-A)
   - **Filtering**: Text input filter with case-insensitive search

3. **Email Column**
   - **Header**: "Email" with up/down arrow and filter icon
   - **Data Type**: Email string
   - **Sorting**: Alphabetical (A-Z, Z-A)
   - **Filtering**: Text input filter with case-insensitive search

4. **Enabled Column**
   - **Header**: "Enabled" with up/down arrow (↕) and filter icon
   - **Data Type**: Boolean
   - **Display**: "true" or "false" text

#### Table Behavior
- **Row Selection**: Clicking a row should highlight it
- **Empty State**: Display "No users found" message when table is empty


## Right Section: New User Form

### Form Header
- **Title**: "New User" at the top of the form
- **Style**: Bold, larger font size

### Form Fields

1. **Username Field**
   - **Type**: Text input
   - **Label**: "Username"
   - **Validation**: Required, alphanumeric characters only
   - **Real-time Validation**: Show error message if invalid

2. **Display Name Field**
   - **Type**: Text input
   - **Label**: "Display Name"
   - **Validation**: Required, 2-50 characters
   - **Real-time Validation**: Show error message if invalid

3. **Phone Field**
   - **Type**: Text input
   - **Label**: "Phone"
   - **Validation**: Optional, phone number format validation
   - **Real-time Validation**: Show error message if invalid format

4. **Email Field**
   - **Type**: Email input
   - **Label**: "Email"
   - **Validation**: Required, valid email format
   - **Real-time Validation**: Show error message if invalid

5. **User Roles Field**
   - **Type**: Dropdown/Select
   - **Label**: "User Roles"
   - **Options**: 
     - Guest
     - Admin
     - SuperAdmin
   - **Default**: No selection
   - **Validation**: Required
   - **Behavior**: Dropdown should open on click, highlight hovered option in blue

6. **Enabled Field**
   - **Type**: Checkbox
   - **Label**: "Enabled"
   - **Default**: Unchecked
   - **Behavior**: Toggle between enabled/disabled user status

### Form Actions

1. **Save User Button**
   - **Style**: Blue button with white text
   - **Position**: Top-right corner of the form
   - **Behavior**: 
     - Validate all required fields
     - Show loading state during submission
     - Display success/error messages
     - Clear form on successful submission
     - Refresh user list to show new user

## Initial Page State

### On Page Load
1. **User List**: Load and display all users or filtered by "Hide Disabled User" setting
2. **Form**: Empty form with default values
3. **Sorting**: Default sort by ID (ascending)

### Data Loading
- **Loading Indicator**: Show spinner while fetching initial user data
- **Error Handling**: Display error message if data cannot be loaded

## Responsive Behavior

### Desktop
- Two-column layout as described above

### Tablet
- Maintain two-column layout with reduced spacing
- Adjust column widths proportionally

### Mobile
- Stack sections vertically
- User list on top, form below
- Table becomes scrollable horizontally
- Form fields stack vertically with full width