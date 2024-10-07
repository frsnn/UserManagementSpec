
# User Management Interface Specification

## Overview
This document provides a detailed specification for the user management screen, focusing on the behavior, components, and user interactions. It will guide developers in implementing the user management UI as described.

---

## Functional Requirements
1. **Add New User:** 
   - Button: `+ New User`
   - When clicked, this button will open the "New User" form on the right side for adding user details.
   
2. **Hide Disabled Users:**
   - Checkbox: `Hide Disabled User`
   - When checked, the table will filter out and hide any users with the `Enabled` field set to `false`.

3. **User Table:**
   - Displays a list of users with the following columns:
     - **ID:** Unique identifier for each user (integer).
     - **User Name:** Username for the user (text).
     - **Email:** User's email address (text).
     - **Enabled:** Boolean field showing whether the user is active (`true`) or disabled (`false`).
   - **Sorting:** Users can sort the table by clicking on the column headers.
   - **Filtering:** Users can filter results by using the input fields under each column header.

4. **New User Form:**
   - Located on the right side of the page.
   - This form is used for entering and saving new user information.
   - The fields in the form are as follows:
     1. **Username:** Text field for entering the user's username.
     2. **Display Name:** Text field for entering the user's display name.
     3. **Phone:** Text field for entering the user's phone number.
     4. **Email:** Text field for entering the user's email address.
     5. **User Roles:** Dropdown for selecting one or multiple roles from available options:
         - `Guest`
         - `Admin`
         - `SuperAdmin`
     6. **Enabled:** Checkbox to enable or disable the user.
   - **Save User Button:** 
     - Button: `Save User`
     - Clicking this button will save the user information entered in the form.

---

## UI Components
1. **Buttons:**
   - `+ New User`: Opens the form to add a new user.
   - `Save User`: Saves the user information.

2. **Checkbox:**
   - `Hide Disabled User`: Toggles the visibility of disabled users in the table.

3. **Table:**
   - Displays the user list with columns for ID, Username, Email, and Enabled status.
   - Sorting and filtering functionalities are available.

4. **Form Fields:**
   - Username, Display Name, Phone, Email, User Roles (dropdown), Enabled (checkbox).

---

## User Flow
1. The user opens the user management page, where all active users are listed.
2. To add a new user, the user clicks the `+ New User` button, which opens the new user form.
3. The user fills in the details (Username, Display Name, etc.) and selects the role(s) from the dropdown.
4. The `Enabled` checkbox determines whether the user is active or disabled.
5. After filling in the form, the user clicks `Save User` to add the user to the system.
6. If the `Hide Disabled User` checkbox is checked, disabled users will no longer appear in the user list.

---

## Behavior
- **Default Behavior:**
  - All users are shown in the table by default, including disabled ones.
  - Users can filter and sort the table using the column headers.
  
- **On Adding New User:**
  - Once the form is filled and `Save User` is clicked, the user is added to the system, and the list refreshes.

- **On Hide Disabled Users:**
  - If the `Hide Disabled User` checkbox is checked, only enabled users are visible in the list.
