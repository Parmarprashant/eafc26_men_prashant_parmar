# PR Title: Feature 04 - Players Management CRUD Dashboard

## PR Description
This PR implements a full CRUD (Create, Read, Update, Delete) dashboard for the Players dataset. It allows administrators to manage the football dataset directly from the frontend UI, integrated with the MongoDB backend.

## Summary of Changes
- Created `playerService.js` for centralized API communication with the backend players endpoints.
- Enhanced `playerSlice.js` with **Redux Toolkit Async Thunks** to handle state management for all CRUD operations.
- Implemented `PlayersList.jsx` page featuring:
  - A responsive **Data Table** displaying player ranks, names, ratings, teams, and nations.
  - **Server-side Pagination** integrated with the backend API.
  - **Search Functionality** to filter players by name, team, or nation.
  - Role-based UI elements (Admin-only "Add" and "Delete" actions).
- Created `PlayerModal.jsx` for a unified **Create and Edit** experience with:
  - Form validation using **Formik** and **Yup**.
  - Dynamic field handling based on the dataset schema.
- Added **Delete Confirmation** dialog to prevent accidental data loss.
- Integrated **Toast notifications** for all data operations (success/error).

## Testing Steps
1. Navigate to the `frontend` directory and run `npm run dev`.
2. Log in as an admin user.
3. Go to the "Players Dataset" module via the sidebar.
4. Verify that the players list loads correctly with pagination.
5. Use the search bar to filter for specific players.
6. Click "Add New Player", fill out the form, and verify it appears in the list.
7. Click the "Edit" icon for a player, modify their details, and verify the update.
8. Click the "Delete" icon, confirm the deletion, and verify the player is removed from the table.

## Notes
- CRUD operations are restricted to users with the 'admin' role in the UI.
- All data is fetched and manipulated in real-time from the MongoDB backend.
