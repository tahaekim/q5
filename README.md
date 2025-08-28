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
