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
