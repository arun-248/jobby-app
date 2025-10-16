# 💼 Jobby App

<div align="center">

[![React](https://img.shields.io/badge/React-18.x-61DAFB?logo=react&logoColor=white&style=for-the-badge)](https://reactjs.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?logo=javascript&logoColor=black&style=for-the-badge)](https://www.javascript.com/)
[![CSS3](https://img.shields.io/badge/CSS3-Responsive-1572B6?logo=css3&logoColor=white&style=for-the-badge)](https://www.w3.org/Style/CSS/)
[![Context API](https://img.shields.io/badge/State-Context%20API-61DAFB?style=for-the-badge)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**A comprehensive job search platform with authentication, advanced filtering, and detailed job listings**

[Live Demo](#) | [GitHub Repo](https://github.com/arun-248/jobby-app)

</div>

---

## 🎯 Test Credentials

**Quick Access - Use these credentials to explore the application:**

* Username: rahul
* Password: rahul@2021

---

## 🌟 Project Highlights

> **Transform Your Job Search**: Browse comprehensive job listings, apply advanced filters, and discover your next opportunity with intelligent job matching and detailed company insights.

**What makes this special:**
- Secure authentication with JWT tokens and protected routes
- Advanced multi-filter system combining employment type, salary, and search
- End-to-end solution from login to job application
- Interactive job browsing with real-time filtering
- Production-ready with professional UI/UX design
- Built for job seekers with real-world employment workflows

---

## 🚀 Key Features

### Authentication & Security
* Secure login system with JWT tokens
* Form validation and error handling
* Protected routes for authenticated users
* Automatic redirect for unauthenticated access
* Session persistence with cookies

### Job Discovery
* Browse comprehensive job listings
* Real-time search functionality
* Filter by employment type (Full-time, Part-time, Freelance, Internship)
* Filter by salary range (10 LPA, 20 LPA, 30 LPA, 40 LPA+)
* Advanced multi-filter combinations
* Dynamic API requests with query parameters

### Profile Management
* User profile display on Jobs page
* Profile image and professional biography
* Professional information display
* Error handling with retry functionality

### Job Details
* Comprehensive job information with descriptions
* Company website links
* Required skills listing with icons
* Company culture and work environment information
* Similar job recommendations
* Detailed employment and location information

### User Experience
* Responsive design for all devices
* Loading states with animated spinners
* Error views with retry options
* No jobs found messaging
* Not found page for invalid routes
* Navigation header with logout functionality

---

## 🏗️ System Architecture

### Data Flow
```
Frontend (React)
      │
      ├─ Login Route → Authentication API
      │
      ├─ Home Route → Welcome Page
      │
      ├─ Jobs Route → Profile API + Jobs API
      │              (with filters)
      │
      ├─ Job Details Route → Job Details API
      │
      └─ Not Found Route → 404 Page
```

### Component Structure
- **Root Components**: App, Header, Home, Login
- **Jobs Section**: Jobs, JobCard, FilterPanel, SearchBar
- **Job Details**: JobDetails, SkillItem, CompanyInfo, SimilarJobItem
- **Common**: Loader, FailureView, NotFound

---

## ⚙️ Tech Stack

### Frontend
- React 18.x with functional components and hooks
- React Router for client-side routing
- Context API for state management
- React Cookies for JWT storage
- CSS3 with responsive design

### API Integration
- Fetch API for HTTP requests
- JWT authentication in request headers
- Query parameters for filtering
- Multi-endpoint data fetching

### Styling & UI
- CSS3 responsive design
- Mobile-first approach
- Flexbox and Grid layouts
- Breakpoints for all device sizes
- React Loader Spinner for loading states
- Bootstrap icons for UI elements

---

## 🌐 API Endpoints

**Authentication**
- POST `/login` - User authentication with credentials

**Profile Data**
- GET `/profile` - User profile information

**Job Listings**
- GET `/jobs` - Job list with filters (employment_type, minimum_package, search)

**Job Details**
- GET `/jobs/:id` - Detailed job information and similar jobs

---

## 🗺️ Application Routes

**Login Route** (`/login`)
- User credential entry
- JWT token generation
- Error message display for invalid credentials
- Redirect to Home on successful login

**Home Route** (`/`)
- Welcome screen for authenticated users
- Call-to-action button to Jobs section
- Hero imagery and branding

**Jobs Route** (`/jobs`)
- Profile information display
- Employment type filters
- Salary range filters
- Search functionality
- Job listing display
- Dynamic filtering with multiple options

**Job Item Details Route** (`/jobs/:id`)
- Detailed job information
- Company details and website link
- Required skills display
- Life at company section
- Similar jobs recommendations
- Error handling with retry

**Not Found Route** (`/not-found`)
- 404 page for invalid URLs
- Navigation back to home

---

## 📊 Data Models

**Employment Types**
- Full Time
- Part Time
- Freelance
- Internship

**Salary Ranges**
- 10 LPA and above
- 20 LPA and above
- 30 LPA and above
- 40 LPA and above

**Filter Combinations**
Multiple filters work together with query parameters combined by commas and logical operators for complex filtering scenarios.

---

## 🚀 Setup & Installation

### Prerequisites
- Node.js 14 or higher
- npm or yarn package manager
- Modern web browser

### Installation Steps

1. Clone the repository
```bash
git clone https://github.com/arun-248/jobby-app.git
cd jobby-app
```

2. Install dependencies
```bash
npm install
```

3. Start development server
```bash
npm start
```

4. Access the application
```
http://localhost:3000
```

---

## 🎨 Design Specifications

**Color Palette**
- Primary: #4f46e5 (Indigo)
- Secondary: #64748b (Slate)
- Dark Background: #272727
- Light Background: #f8fafc
- Accent: #fbbf24 (Amber)

**Responsive Breakpoints**
- Mobile: < 576px
- Small: 576px - 768px
- Medium: 768px - 992px
- Large: 992px - 1200px
- Extra Large: > 1200px

**Typography**
- Font Family: Roboto
- Scalable font sizes across breakpoints

---

## 🔥 Advanced Features

**Authentication Flow**
- Login form submits to authentication API
- JWT token stored in cookies on success
- Token validated for protected routes
- Automatic redirect based on auth status
- Logout clears session

**Multi-Filter System**
- Employment type filters as comma-separated string
- Salary range sent as single parameter
- Search term handled separately
- Combined query parameters in API calls
- Real-time filter updates

**Search Implementation**
- Search icon button triggers API call
- Query parameter updates dynamically
- Loader displayed during fetch
- Results updated automatically

**Error Handling**
- Retry buttons for failed API calls
- User-friendly error messages
- Failure views for different scenarios
- Graceful degradation

---

## 🎓 Learning Outcomes

### React Concepts
- Functional components and hooks
- Context API for state management
- React Router for navigation
- Form handling and validation
- API integration patterns

### Advanced Patterns
- Protected routes with authentication
- Query parameter management
- Multi-filter implementation
- Loading and error states
- Responsive component design

### Development Skills
- API consumption and data transformation
- Authentication and security basics
- State management strategies
- Component composition
- User experience considerations

---

## 🛠️ Troubleshooting

**Login Issues**
- Verify correct credentials
- Check browser cookie settings
- Ensure HTTPS for production

**API Failures**
- Verify internet connection
- Check API endpoint availability
- Confirm JWT token validity
- Review browser console for errors

**Rendering Issues**
- Clear browser cache
- Check responsive design at current breakpoint
- Verify component props

---

## 📈 Future Roadmap

### Short-term Goals (Next 3 months)
- Save/bookmark favorite jobs
- Apply directly through app
- Advanced search with keywords
- Job alerts and notifications
- View application history
- Enhanced profile settings
- Dark/light theme toggle

### Long-term Vision (6-12 months)
- Resume upload and management
- Interview preparation tools
- Salary comparison tool
- Company reviews and ratings
- Networking features
- Mobile app version
- Real-time job notifications
- AI-powered job recommendations

---

## ♿ Accessibility & Best Practices

- Semantic HTML structure
- Alt text for all images
- ARIA labels where appropriate
- Keyboard navigation support
- Color contrast compliance
- Form validation feedback
- Error message clarity

---

## ⚡ Performance Considerations

- Optimized API requests with proper caching
- Lazy loading of components
- Efficient state updates
- Image optimization
- Responsive image loading

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

**Reporting Bugs**
1. Check existing issues first
2. Create detailed bug report
3. Include steps to reproduce
4. Add screenshots if possible

**Suggesting Features**
1. Open a discussion on GitHub
2. Describe the feature clearly
3. Explain the use case
4. Consider implementation complexity

**Pull Requests**
1. Fork the repository
2. Create feature branch (git checkout -b feature/AmazingFeature)
3. Commit changes (git commit -m 'Add AmazingFeature')
4. Push to branch (git push origin feature/AmazingFeature)
5. Open Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

```
MIT License - Free to use, modify, and distribute
Open source and community-driven
```

---

## 🙏 Acknowledgments

- React community for documentation and tools
- Job API for providing job data
- Design system for color palette
- Open source community for inspiration and support

---


<div align="center">

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License - Feel free to use, modify, and distribute
Open source and ready for collaboration
```

**💼 Built with passion for career development | 🚀 Powered by React**

*Made with ❤️ by [Arun Chinthalapally](https://github.com/arun-248)*

</div>
