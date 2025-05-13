# Belleville Dental Website Documentation

## Table of Contents
- [User Guide](#user-guide)
  - [Getting Started](#getting-started)
  - [Features Overview](#features-overview)
  - [Navigation Guide](#navigation-guide)
  - [Interactive Features](#interactive-features)
  - [Troubleshooting](#troubleshooting)
- [Developer Guide](#developer-guide)
  - [Project Architecture](#project-architecture)
  - [Tech Stack](#tech-stack)
  - [Component Structure](#component-structure)
  - [Development Setup](#development-setup)
  - [Deployment](#deployment)

## User Guide

### Getting Started

The Belleville Dental website is a modern, responsive dental practice website that provides information about dental services, educational resources, and product offerings.

#### System Requirements
- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Minimum screen resolution: 320px width

### Features Overview

1. **Homepage**
   - Hero section with practice introduction
   - Image gallery showcasing the facility
   - FAQ section with common patient questions
   - Contact form for inquiries

2. **Research Section**
   - Clinical studies information
   - Technology innovation updates
   - Research statistics and impact metrics
   - Educational video content

3. **Education Portal**
   - Patient education resources
   - Professional development materials
   - Workshop information
   - Community programs

4. **Products Catalog**
   - Dental care products listing
   - Product ratings and reviews
   - Price information
   - Product descriptions and images

5. **About Us**
   - Practice mission and values
   - Team information
   - Facility details
   - Commitment to excellence

### Navigation Guide

- **Main Navigation**: Use the top navigation bar to access primary sections
- **Hash Links**: Click on footer links for quick access to specific sections
- **Responsive Menu**: On mobile devices, use the hamburger menu for navigation
- **Scroll to Top**: Automatic scroll to top when changing pages

### Interactive Features

1. **Product Ratings**
   - Click on stars to rate products (1-5 stars)
   - Ratings are saved locally
   - View average ratings from all users

2. **Contact Form**
   - Fill in name, email, and message
   - Form validation ensures proper input
   - Receive confirmation upon submission

3. **FAQ Section**
   - Click questions to expand/collapse answers
   - Interactive accordion-style interface

### Troubleshooting

Common Issues and Solutions:

1. **Images Not Loading**
   - Refresh the page
   - Check internet connection
   - Clear browser cache

2. **Contact Form Issues**
   - Ensure all required fields are filled
   - Check email format
   - Try using a different browser

3. **Rating System Not Working**
   - Enable JavaScript
   - Clear browser storage
   - Try private browsing mode

## Developer Guide

### Project Architecture

```
belleville-dental/
├── public/               # Static assets
│   ├── products/        # Product images
│   ├── gallery/         # Gallery images
│   └── ...
├── src/
    ├── components/      # React components
    ├── assets/          # Fonts and documents
    └── helper/          # Utility functions

```

### Tech Stack

1. **Frontend Framework**
   - React 19
   - Vite 6.3
   - Framer Motion 12.10

2. **Styling**
   - CSS Modules
   - Bootstrap 5.3
   - Custom responsive design system

3. **State Management**
   - React Hooks
   - Local Storage for persistence

4. **Routing**
   - React Router 7.5
   - Hash Link for smooth scrolling

### Component Structure

1. **Layout Components**
   - `Navbar`: Main navigation
   - `Footer`: Site-wide footer
   - `ScrollToTop`: Navigation utility

2. **Page Components**
   - `Hero`: Homepage hero section
   - `Research`: Research page
   - `Education`: Education portal
   - `Products`: Product catalog
   - `AboutUs`: About page

3. **Shared Components**
   - `LCard`: Large card component
   - `FAQContactUs`: FAQ and contact section
   - `Gallery`: Image gallery

### Development Setup

1. **Prerequisites**
   ```bash
   - Node.js 18+
   - npm 9+
   ```

2. **Installation**
   ```bash
   npm install
   ```

3. **Development Server**
   ```bash
   npm run dev
   ```

4. **Build**
   ```bash
   npm run build
   ```

### Environment Variables
```env
VITE_APP_TITLE=Belleville Dental
```

### Development Workflow

1. **Code Style**
   - Use ESLint configuration
   - Follow React best practices
   - Maintain component modularity

2. **Performance Considerations**
   - Lazy load images
   - Optimize bundle size
   - Use proper caching strategies

3. **Responsive Design**
   - Mobile-first approach
   - Fluid typography
   - Breakpoint system

### Deployment

The project uses Vercel for deployment with the following configuration:

```json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/" }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "Cache-Control", "value": "public, max-age=0, must-revalidate" }
      ]
    }
  ]
}
```


# Bellevielle Dental (shortened)

## Project Overview
This Single Page Application SPA Webpage includes:

* **Navigation Bar**: Main site navigation with links to Research, About Us, Education, and Products sections
* **Hero Section**: Attention-grabbing hero area with "SMILE BRIGHTER" headline.
* **Responsive Design**: Fully responsive layout that scales appropriately across different device sizes

### Technical Details

* Built with **React 19** and **Vite**
* Uses **Bootstrap** **5** for baseline styling
* Implements **React** **Router** for navigation
* Features completely responsive design using CSS variables and relative sizing
* Typography using **Poppins** font family (multiple weights: 300, 400, 500, 600, 700, 800, 900)
* Custom responsive components built from scratch

### Responsive Design Approach
The site uses a clever responsive design strategy:

* All measurements are relative to a 1920px base width
* CSS variables and `calc()` functions create a fluid layout that scales proportionally
* Media queries handle layout changes on smaller devices

### Getting Started
1. Clone this repository
2. Install dependencies: `npm install`
3. Run development server: `npm run dev`
4. Build for production: `npm run build`

### Project Structure
* components - React component (Navbar, Hero)
* fonts - Poppins font files
* public - Static assets like images
