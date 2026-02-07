# BloggerBro

BloggerBro is a full-stack blog platform built with Next.js (App Router) and MongoDB. It provides a public blog feed with category filtering, individual blog detail pages, and an admin area for creating and managing posts.

## Features

- Public blog feed with category filters (All, Technology, Startup, Lifestyle)
- Blog detail pages with author info and hero image
- Admin area UI with sidebar, top bar, and notifications
- Create blog posts with image upload stored in `/public`
- Blog management view with refresh and listing
- REST API endpoints for blog creation and retrieval

## Tech Stack

- Framework: Next.js 15 (App Router)
- UI: React 19, Tailwind CSS v4
- Database: MongoDB with Mongoose
- HTTP: Axios
- Notifications: React Toastify

## Project Structure (High Level)

```
app/
  page.js                    # Public homepage
  blogs/[id]/page.jsx         # Blog details
  admin/
    layout.jsx                # Admin layout with sidebar + toast
    addProduct/page.jsx       # Create blog post
    blogList/page.jsx         # Manage/list blogs
    subscriptions/page.jsx    # Placeholder
  api/
    blog/route.js             # GET list + POST create
    blog/[id]/route.js        # GET by id
lib/
  config/db.js                # MongoDB connection
  models/BlogModel.js         # Blog schema
Components/                   # Reusable UI components
Assets/                       # Images and icons
```

## Routes

### Public

- / - Blog feed
- /blogs/[id] - Blog details

### Admin

- /admin/addProduct - Add blog post
- /admin/blogList - List/manage posts
- /admin/subscriptions - Placeholder page
- /admin - Placeholder page

### API

- GET /api/blog - List all blogs
- GET /api/blog?id=<id> - Get blog by query param
- GET /api/blog/[id] - Get blog by route param
- POST /api/blog - Create blog with multipart form data

## Data Model

BlogModel (Mongoose):

- title (String, required)
- description (String, required)
- category (String, required)
- author (String, required)
- image (String, required, stored as URL path)
- authorImg (String, required)
- date (Date, default: now)

## Environment Setup

This project currently connects to MongoDB in `lib/config/db.js`.
For production or sharing, use an environment variable.

.env.local
```
MONGODB_URI=your_mongodb_connection_string
```

Then update `lib/config/db.js` to read from `process.env.MONGODB_URI`.

## Install and Run

```bash
npm install
npm run dev
```

Open http://localhost:3000

## API Usage Examples

### Get all blogs

```bash
curl http://localhost:3000/api/blog
```

### Create a blog (multipart)

```bash
curl -X POST http://localhost:3000/api/blog \
  -F "title=My Blog Title" \
  -F "description=My blog content..." \
  -F "category=Technology" \
  -F "author=Your Name" \
  -F "authorImg=/author_img.png" \
  -F "image=@/path/to/thumbnail.jpg"
```

## Notes

- Uploaded images are saved in `/public` with a timestamped filename.
- The admin "Delete" button is UI-only (API delete not implemented yet).
- The blog detail page currently renders the description plus placeholder sections.

## Scripts

- npm run dev - Start dev server
- npm run build - Build for production
- npm run start - Start production server
- npm run lint - Run linting

