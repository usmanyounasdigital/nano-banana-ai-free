# Nano Banana AI - Complete Web Application

A professional Next.js web application that clones the nanobananaai.org website with full functionality, including an admin panel and content management system.

## Features

### Frontend
- **Modern Design**: Responsive design with Tailwind CSS
- **Homepage**: Complete clone of nanobananaai.org with all sections
- **Blog System**: Dynamic blog with posts fetched from database
- **Navigation**: Professional header and footer components
- **Mobile Responsive**: Works perfectly on all devices

### Admin Panel & CMS
- **Secure Authentication**: JWT-based login system
- **Dashboard**: Overview of posts and statistics
- **Blog Management**: Create, edit, delete, and publish blog posts
- **Rich Content Editor**: HTML support for blog content
- **User Management**: Admin user system

### Technical Stack
- **Framework**: Next.js 14 with TypeScript
- **Styling**: Tailwind CSS
- **Database**: SQLite with custom ORM
- **Authentication**: JWT tokens with bcrypt password hashing
- **API**: RESTful API routes built into Next.js

## Installation & Setup

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Start Development Server**
   ```bash
   npm run dev
   ```

3. **Access the Application**
   - Frontend: http://localhost:3000
   - Admin Panel: http://localhost:3000/admin/login

## Default Admin Credentials

- **Username**: admin
- **Password**: admin123

## Project Structure

```
src/
├── app/
│   ├── admin/           # Admin panel pages
│   ├── api/             # API routes
│   ├── blog/            # Blog pages
│   └── page.tsx         # Homepage
├── components/          # Reusable components
├── lib/                 # Utilities and database
└── types/               # TypeScript types
```

## Admin Panel Features

### Dashboard
- Post statistics and overview
- Quick actions for content management

### Blog Management
- Create new blog posts with rich content editor
- Edit existing posts
- Publish/unpublish posts
- Delete posts
- SEO-friendly slug generation

### Content Management
- HTML content support
- Featured image URLs
- Author management
- Publication status control

## API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Blog Posts
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post
- `GET /api/posts/[id]` - Get specific post
- `PUT /api/posts/[id]` - Update post
- `DELETE /api/posts/[id]` - Delete post

## Database Schema

### Users Table
- id, username, email, password, role, created_at

### Posts Table
- id, title, slug, content, excerpt, author, image, published, created_at, updated_at

### Pages Table
- id, title, slug, content, published, created_at, updated_at

## Deployment

The application is ready for deployment on platforms like Vercel, Netlify, or any Node.js hosting service.

### Build for Production
```bash
npm run build
```

### Start Production Server
```bash
npm start
```

## Customization

The application is built with modularity in mind:

- **Styling**: Modify Tailwind classes in components
- **Content**: Use the admin panel to manage all content
- **Features**: Add new pages by creating files in the `app/` directory
- **Database**: Extend the schema in `src/lib/db/database.ts`

## Security Features

- Password hashing with bcrypt
- JWT token authentication
- Protected admin routes
- SQL injection prevention
- XSS protection

## License

This project is created for educational and demonstration purposes.

---

**Note**: This is a complete clone of nanobananaai.org with additional CMS functionality. All content and design elements are recreated for demonstration purposes.

