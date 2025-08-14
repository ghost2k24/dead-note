# Death Note - One Entry Per User System

## Overview
This is a Death Note themed web application where each user can only submit one entry to the Death Note notebook. After submitting their entry, users become spectators and can only view other users' entries.

## How It Works

### 1. User Entry Process
- Users start at `note.html` and click "Take Pen" to access the Death Note
- In `murder.html`, users enter their nickname and fill out the form:
  - Victim name
  - Kill method
- Each nickname can only be used once
- After submission, users cannot submit another entry

### 2. User State Management
- **New User**: Can fill out and submit the Death Note form
- **Returning User (No Entry)**: Can still submit their first entry
- **Returning User (Has Entry)**: Can only view the Death Note records

### 3. Data Storage
- All entries are stored in `localStorage` under the key `deathNoteRecords`
- User's current nickname is stored under `currentUserNick`
- Each entry contains: nickname, victim, method, and timestamp

### 4. Viewing Records
- Users can view all Death Note entries in `records.html`
- Entries are paginated (20 per page)
- Users can navigate back to the Death Note from the records page

## Files Structure

- `note.html` - Entry point, "Take Pen" button
- `murder.html` - Main form for Death Note entries
- `records.html` - View all Death Note entries
- `style-*.css` - Styling for each page
- Audio files for atmospheric background

## Features

✅ **One Entry Per User**: Each nickname can only submit once  
✅ **Persistent Storage**: Entries saved in localStorage  
✅ **User State Detection**: Automatically detects if user has already submitted  
✅ **Pagination**: Browse through all entries easily  
✅ **Responsive Design**: Works on different screen sizes  
✅ **Death Note Theme**: Atmospheric styling and audio  

## Testing

For development/testing purposes, a "Clear Data" button appears when running on localhost. This allows you to reset the user state and test the flow multiple times.

## Browser Compatibility

- Modern browsers with localStorage support
- Audio autoplay may be blocked by some browsers
- Responsive design works on mobile and desktop

## Future Enhancements

- Server-side storage for persistence across devices
- User authentication system
- Entry editing/deletion (admin only)
- Search and filter functionality
- Export Death Note data
