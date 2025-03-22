# Roadmap

## Prompt

Build a mobile app that allows users to find GPS locations where other community members have pin pointed places where they found different types of berries (the fruit).

## Main Features

### New post screen

- Select photos from gallery. A grid of 4 columns of images with a preview on the top. You can select multiple images by tapping on the image. There is a small circle on the top left corner of each image on the gallery grid.
- Add new berries Post with GPS location and photo(s), caption, a list of Fruit tags
- The location is a text field of the place name or the GPS coordinates.
- Share post with friends via NativeShare

### Main screen

- View all posts in a list feed / stream
- View post details including photos, static map, caption, and location, date, name of the user who posted it.
- You can see the number of likes and comments on the post.
- You can like, comment, and share a post
- There is 3 dot menu on the top right corner of the post to report the post. It's a dropdown menu

### Technologies

- React Native
- Expo
- Expo Router
- Safe Area Context
- Supabase and Drizzle
- TypeScript
- NativeWind
- Next-Auth
- `expo-image-picker`

### Database schema

### Later

- Tag friends on posts
- User registration and login
- Map View:
  * Interactive map showing fruit locations
  * Clustering for dense areas
  * Filters by fruit type, recency, and popularity
  * Current location search
- Notifications for new berries in nearby areas

---

## Prompt (improved by Bolt.new, Claude 3.7 thinking and o3-mini)

Create a React Native mobile app called "Berry Map" with the following specifications:

It's a berry foraging app using React Native and Expo, implementing these core features:

1. Post Creation Screen:
- Implement a photo selector with a 4-column grid layout
- Enable multi-photo selection with small circular indicators
- Photo upload (min 1, max 6 photos). Upload to Supabase storage
- Provide feedback for upload progress and errors.
- In the next screen
  - Include fields for:
    * GPS coordinates/location name (required). Use location services; ask for Precise permissions
    * Caption, A textarea field (max 500 characters)
    * Allow users to pick one (or multiple) from predefined tags of Fruit.
  - Include form validation and error handling
    - Ensure mandatory fields are filled and enforce character limits. Show user-friendly error messages.

2. Feed Screen:
- Display post stream with:
  * User name
  * Date posted
  * Location name and country
  * A carousel with a static map alongside the photos
  * Number of likes and comments
- Implement post interactions:
  * Like/unlike functionality
  * Comment section. Display last comment.
  * Share capability
  * Report option (under 3-dot menu) with confirmation
- Add pull-to-refresh
- Add infinite scroll for lazy loading posts as the user scrolls. Use `@shopify/flash-list`

Technical Requirements:
- Stack:
  * React Native with Expo SDK
  * Expo Router for navigation
  * TypeScript for type safety
  * NativeWind for styling
  * Supabase/Drizzle for backend
  * Next-Auth for authentication
  * Safe Area Context
  * State Management: zustand
- Ensure proper handling of:
  * Offline state
  * Loading states
  * Location permissions
- Permissions:
  - Handle location permissions explicitly, with guidance for denied or restricted access.
- Error Handling:
  - Clear and user-friendly error messages for both form validation and network issues.

Deliverable: A fully functional mobile app that enables users to share and discover berry foraging locations while maintaining a responsive
