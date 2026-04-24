# BloggerBro

BloggerBro is a modern blog platform built with Next.js 15 (App Router) and React 19. It provides a clean, responsive interface for viewing and browsing blog posts with a beautiful blog feed and detailed blog pages.

## Features

- Responsive blog feed displaying all blog posts
- Individual blog detail pages with full post content
- Blog post list component with blog items
- Clean and modern UI with Tailwind CSS
- Static blog data with easy extensibility

## Tech Stack

- Framework: Next.js 15 (App Router)
- UI: React 19, Tailwind CSS v4
- Styling: PostCSS
- Language: JavaScript/JSX

## Project Structure

```
app/
  layout.js              # Root layout
  page.js                # Homepage with blog list
  blogs/
    [id]/
      page.jsx           # Individual blog detail page
Components/
  BlogItem.jsx           # Single blog item component
  BlogList.jsx           # Blog list container
  Header.jsx             # Header component
  Footer.jsx             # Footer component
Assets/
  assets.js              # Assets configuration
public/                  # Static files and images
```

## Routes

- `/` - Homepage with blog list
- `/blogs/[id]` - Individual blog detail page

## Getting Started

### Prerequisites

- Node.js 18.0 or higher
- npm or yarn

### Installation and Setup

1. Clone the repository:
```bash
git clone https://github.com/prosanto0das/BloggerBro-.git
cd BloggerBro-
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:3000`

## Available Scripts

- `npm run dev` - Start development server (port 3000)
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint checks

## Project Notes

- Blog data is currently stored statically. The project can be extended to use a database in the future.
- Components are located in the `Components/` directory with capital 'C'.
- Assets are managed through the `Assets/assets.js` file.
- The application uses Next.js 15's App Router for modern routing.

## License

This project is open source and available for use.

