# BloggerBro

A modern, responsive blog platform built with **Next.js 15** and **React 19**. BloggerBro provides a beautiful, intuitive interface for reading and discovering blog posts across multiple categories including Technology, Startup, and Lifestyle.

## 🌟 Features

- **Responsive Blog Feed** - Browse all blog posts with category-based filtering (All, Technology, Startup, Lifestyle)
- **Category Filtering** - Easily filter posts by category with interactive buttons
- **Blog Detail Pages** - View full blog posts with author information, featured images, and structured content
- **Author Information** - Each blog includes author name and profile image
- **Email Subscription** - Newsletter subscription form on the homepage
- **Beautiful UI** - Modern, clean design with Tailwind CSS and custom styling
- **Dynamic Routing** - URL-based navigation for individual blog posts using Next.js dynamic routes
- **Static Blog Data** - Pre-configured blog posts ready to display

## 🛠️ Tech Stack

- **Framework**: Next.js 15 (App Router)
- **UI Library**: React 19
- **Styling**: Tailwind CSS v4 with PostCSS
- **Image Optimization**: Next.js Image component
- **Language**: JavaScript/JSX

## 📁 Project Structure

```
BloggerBro-/
├── app/                           # Next.js App Router directory
│   ├── layout.js                 # Root layout wrapper
│   ├── page.js                   # Homepage with Header, BlogList, Footer
│   ├── blogs/
│   │   └── [id]/
│   │       └── page.jsx          # Blog detail page (dynamic route)
│   ├── globals.css               # Global styles
│   └── favicon.ico
├── Components/                    # React components
│   ├── Header.jsx                # Navigation & hero section with email subscription
│   ├── BlogList.jsx              # Blog list with category filters
│   ├── BlogItem.jsx              # Individual blog card component
│   └── Footer.jsx                # Footer with social links
├── Assets/                        # Static images and data
│   ├── assets.js                 # Images and blog data (16 sample blogs)
│   ├── logo.png, logo_light.png  # Branding logos
│   ├── blog_pic_*.png            # Blog thumbnail images (1-16)
│   ├── profile_icon.png          # Author profile placeholder
│   └── social icons              # Facebook, Twitter, Google+ icons
├── public/                        # Public static files
├── package.json                  # Dependencies & scripts
└── README.md                      # This file
```

## 🚀 Routes

| Route | Description |
|-------|-------------|
| `/` | Homepage - displays blog feed with category filters |
| `/blogs/[id]` | Blog detail page - shows full blog post with author info |

## 💾 Data Model

Each blog post includes:
```javascript
{
  id: Number,           // Unique identifier
  title: String,        // Blog post title
  description: String,  // Blog excerpt/preview
  image: Image,         // Thumbnail image
  date: Date,           // Publication date
  category: String,     // Category: "Technology", "Startup", or "Lifestyle"
  author: String,       // Author name (currently "Alex Bennett")
  author_img: Image     // Author profile image
}
```

The project includes **16 sample blog posts** across all categories in `Assets/assets.js`.

## 🎨 Key Components

### Header
- Logo and "Get Started" button
- Hero section with title and tagline
- Email subscription form

### BlogList
- Category filter buttons (All, Technology, Startup, Lifestyle)
- Dynamic filtering of blog posts
- Responsive grid layout

### BlogItem
- Blog thumbnail with category badge
- Title and description preview
- "Read more" link with arrow icon
- Hover shadow effect for better UX

### Blog Detail Page
- Blog header with author info and profile image
- Featured blog image
- Full blog content with sections
- Links back to homepage

## 🏃 Getting Started

### Prerequisites
- Node.js 18.0 or higher
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/prosanto0das/BloggerBro-.git
cd BloggerBro-
```

2. **Install dependencies**
```bash
npm install
```

3. **Start development server**
```bash
npm run dev
```

4. **Open in browser**
Navigate to `http://localhost:3000`

## 📝 Available Scripts

```bash
npm run dev      # Start development server (hot reload on port 3000)
npm run build    # Build optimized production bundle
npm run start    # Start production server
npm run lint     # Run ESLint to check code quality
```

## 🔧 Customization

### Adding New Blog Posts
Edit `Assets/assets.js` and add a new object to the `blog_data` array:
```javascript
{
  id: 17,
  title: "Your Blog Title",
  description: "Blog preview text...",
  image: import_your_image_here,
  date: Date.now(),
  category: "Technology", // or "Startup", "Lifestyle"
  author: "Author Name",
  author_img: profile_icon
}
```

### Updating Blog Detail Content
Edit the template sections in `app/blogs/[id]/page.jsx` to customize how full blog posts are displayed. Currently includes Introduction and Steps sections as examples.

### Styling
- Global styles: `app/globals.css`
- Component styling: Tailwind CSS classes inline with components
- Custom shadows and effects defined in component className attributes

## 📋 Blog Categories

The platform supports three main categories:
- **Technology** - Programming, software development, tech trends
- **Startup** - Entrepreneurship, business growth, startup strategies
- **Lifestyle** - Personal development, wellness, lifestyle tips

## 🌐 Deployment

This Next.js application can be easily deployed on:
- **Vercel** (recommended - official Next.js platform)
- **Netlify**
- **AWS**
- **Docker containers**
- **Traditional Node.js hosting**

## 📄 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

Created and maintained by prosanto0das

---

**Made with ❤️ using Next.js and React**

