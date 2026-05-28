# PR Title: Feature 05 - Analytics Dashboard & Dynamic Admin Overview

## PR Description
This PR implements the Analytics Dashboard module and converts the static Dashboard overview into a dynamic, data-driven system. It leverages MongoDB aggregation APIs to visualize dataset trends and provides real-time system statistics for administrators.

## Summary of Changes
- Created `statsService.js` to interface with the backend analytics and aggregation endpoints.
- Implemented **Analytics Dashboard** (`Analytics.jsx`) featuring:
  - **Summary Cards**: Total players, average rating, highest rating, and average pace.
  - **Position Distribution**: A Pie chart visualizing the player count across different field positions.
  - **Nation Analytics**: A Bar chart showing the top 10 countries represented in the dataset.
  - **Top Teams**: A Bar chart comparing the average ratings of the top 10 football clubs.
- Updated **Main Dashboard** (`Dashboard.jsx`) to be dynamic:
  - Fetches real-time stats (Total Users, Deleted Records, Latest Additions) via the Admin API.
  - Displays a list of the 5 most recently added players.
  - Shows system health and environment status.
- Integrated **Recharts** library for all data visualizations.
- Added smooth fade-in animations for all analytics components.

## Testing Steps
1. Navigate to the `frontend` directory and run `npm run dev`.
2. Log in as an admin to see the full dynamic dashboard overview.
3. Navigate to the "Analytics" module via the sidebar.
4. Verify that all charts load correctly and display tooltips on hover.
5. Check the summary cards for accurate data reflecting the MongoDB collection.

## Notes
- The Analytics page is available to both Users and Admins, while the detailed overview stats are tailored for Admin users.
- Charts are fully responsive and adapt to different screen sizes.
