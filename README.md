# Accredited Assistance Association (AAA)

## Project Overview

**Accredited Assistance Association (AAA)** is a comprehensive digital marketplace platform designed specifically to address the service discovery and trust challenges in Pakistan's local business ecosystem. In Pakistan, most local service providers lack proper digital platforms to showcase their services, creating significant challenges for customers who struggle to find reliable and verified service providers in their local areas. Additionally, there's no centralized platform for customers to communicate directly with service providers, and the absence of transparent review and rating systems for local services makes it difficult to discover trustworthy services beyond immediate neighborhood knowledge.

Accredited Assistance Association (AAA) provides a comprehensive solution that bridges the gap between service providers and customers in Pakistan by offering easy service discovery through category and location browsing, access to verified and trustworthy service providers, transparent reviews and ratings from other customers, real-time messaging with service providers, and structured complaint management systems. For service providers, the platform offers a professional space to create detailed business profiles with service listings, direct communication with potential and existing customers, review management capabilities, business analytics to track inquiries and customer interactions, and increased visibility in the local service market.

## Key Features

### Authentication & User Management
- **Multi-Provider Authentication**: Email/password, Google OAuth, Facebook OAuth
- **Role-Based Access**: Separate dashboards for customers, businesses, and administrators
- **Secure Sessions**: JWT-based authentication with MongoDB session storage
- **Password Management**: Forgot password and reset functionality with email verification

### User Profiles & Business Management
- **Customer Profiles**: Personal profiles with contact information and preferences
- **Business Profiles**: Comprehensive business profiles with:
  - Service categories and descriptions
  - Contact information and business hours
  - Professional photos and galleries
  - Service area coverage
  - Business verification status

### Service Discovery & Search
- **Category-Based Browsing**: Organized service categories for easy navigation
- **Advanced Search**: Search by service type, location, and business name
- **Service Provider Directory**: Comprehensive listing of all registered businesses
- **Location-Based Results**: Find services in specific geographic areas

### Reviews & Ratings System
- **Customer Reviews**: Detailed review system with ratings (1-5 stars)
- **Review Management**: Businesses can respond to reviews
- **Review Moderation**: Admin oversight for review quality and authenticity
- **Review Analytics**: Track review trends and customer satisfaction

### Real-Time Messaging System
- **Direct Communication**: 1:1 messaging between customers and businesses
- **Real-Time Updates**: Socket.IO powered instant messaging
- **Message Features**:
  - Text messaging
  - Typing indicators
  - Message read receipts
  - Message deletion
  - Business room management
- **Message History**: Persistent message storage and retrieval

### Complaint & Inquiry Management
- **Structured Complaints**: Formal complaint submission system
- **Inquiry System**: General inquiry form for service information
- **Email Notifications**: Automated email alerts for new complaints/inquiries
- **Admin Dashboard**: Comprehensive complaint management interface
- **Resolution Tracking**: Track complaint status and resolution progress

### Admin Dashboard & Management
- **User Management**: Admin control over user accounts and permissions
- **Business Management**: Approve, modify, or remove business listings
- **Complaint Management**: Review and manage customer complaints
- **Service Category Management**: Add, edit, or remove service categories
- **Analytics Dashboard**: Overview of platform usage and statistics

### Email Services
- **Automated Notifications**: Email alerts for various platform activities
- **Password Reset**: Secure password reset via email
- **Account Verification**: Email verification for new accounts
- **Complaint Notifications**: Email alerts for complaint submissions

### Security Features
- **Rate Limiting**: API rate limiting to prevent abuse
- **Helmet Security**: Security headers and CSP protection
- **Input Validation**: Comprehensive input validation and sanitization
- **Session Security**: Secure session management with MongoDB storage
- **CORS Protection**: Configured CORS for secure cross-origin requests

## Screenshots

### Platform Overview
![Homepage](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/Homepage.png)

### Customer Login
![Customer Login](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/customer%20login.png)
### Customer Dasbhoard
![Customer Dashboard](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/customerdasbhoard.png)

### Business Dashboard
![Business Dashboard](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/Bsuiness%20DAsbhoard.png)

### Admin Dashboard
![Admin Dashboard](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/Admin%20Dashboard.png)

### Service Discovery
![Services Cards](https://github.com/gct-bsit-2021/accredited-assistance-association/blob/main/Front%20End/public/Servicescards.png)

## Technology Stack

| Category | Technology | Description |
|----------|------------|-------------|
| **Backend** | Node.js | JavaScript runtime for server-side development |
| | Express.js | Web application framework for Node.js |
| | MongoDB | NoSQL database for data storage |
| | Mongoose | MongoDB object modeling for Node.js |
| | Passport.js | Authentication middleware for Node.js |
| | JWT | Secure token-based authentication |
| | Socket.IO | Real-time bidirectional event-based communication |
| | Nodemailer | Email sending library for Node.js |
| | Helmet | Security middleware for Express applications |
| | express-rate-limit | Rate limiting middleware |
| | express-session | Session management middleware |
| | connect-mongo | MongoDB session store for Express |
| **Frontend** | React 18 | Modern JavaScript library for building user interfaces |
| | React Router | Declarative routing for React applications |
| | React Hook Form | Performant forms with easy validation |
| | React Query | Data fetching and caching library |
| | React Toastify | Beautiful toast notifications |
| | Slick Carousel | Responsive carousel component |
| | CSS3 | Modern styling with responsive design |
| | JavaScript ES6+ | Modern JavaScript features |
| **Development** | Create React App | React application boilerplate |
| | Nodemon | Development tool for Node.js applications |
| | GitHub Pages | Static site hosting for frontend |
| | Environment Variables | Secure configuration management |
| | PM2 | Process manager for production Node.js applications |
| **Database** | MongoDB Atlas | Cloud database service |
| | MongoDB Local | Local development database |
| | GridFS | File storage for images and documents |
| | MongoDB Sessions | Session storage in database |

## Project Structure

```
Accredited-Assistant-Association/
├── Back-End/
│   └── server/
│       ├── config/           # Database configuration, Passport strategies
│       ├── middleware/       # Authentication middleware
│       ├── models/           # Mongoose models (User, Business, Review, etc.)
│       ├── routes/           # REST API routes
│       │   ├── admin.js      # Admin management routes
│       │   ├── auth.js       # Authentication routes
│       │   ├── business.js   # Business management routes
│       │   ├── complaints.js # Complaint handling routes
│       │   ├── messaging.js  # Messaging system routes
│       │   ├── review.js     # Review system routes
│       │   └── users.js      # User management routes
│       ├── services/         # Email service and utilities
│       ├── socket.js         # Socket.IO server configuration
│       └── server.js         # Express application entry point
│
└── Front End/
    ├── public/               # Static assets and HTML template
    └── src/
        ├── components/       # Reusable UI components
        │   ├── AdminComplaintsDashboard.js
        │   ├── BusinessMessagingDashboard.js
        │   ├── ChatWindow.js
        │   ├── ComplaintForm.js
        │   └── [Other components]
        ├── context/          # React Context providers
        │   ├── AuthContext.js
        │   ├── SocketContext.js
        │   └── AdminContext.js
        ├── pages/            # Route-level page components
        │   ├── Home.js
        │   ├── BusinessDirectory.js
        │   ├── AdminDashboard.js
        │   └── [Other pages]
        ├── utils/            # Utility functions and helpers
        └── styles/           # CSS stylesheets
```

## Getting Started

### Quick Setup (Essentials Only)

1) Backend
```bash
cd Back-End/server
npm install
```

Create `Back-End/server/.env` with at least:
```env
MONGO_URI_LOCAL=mongodb://localhost:27017/aaa_services  # or use MONGO_URI for Atlas
JWT_SECRET=<secure-random-string>
SESSION_KEY=<secure-random-string>
PORT=5000
FRONTEND_URL=http://localhost:3000
NODE_ENV=development
```

Run the API:
```bash
npm run dev
```

2) Frontend
```bash
cd "Front End"
npm install
npm start
```

3) Database (MongoDB)
- Local: install MongoDB and ensure it runs on port 27017, then use `MONGO_URI_LOCAL`.
- Atlas: create a free cluster, add a DB user and IP whitelist, then set `MONGO_URI`.

Health checks:
- API: http://localhost:5000/ and http://localhost:5000/api/status
- App: http://localhost:3000

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user info

### User Management
- `POST /api/users/register` - Register new user
- `POST /api/users/login` - User login
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile
- `PUT /api/users/profile-picture` - Update profile picture
- `PUT /api/users/change-password` - Change password

### Business Management
- `POST /api/business` - Create business profile
- `GET /api/business` - Get all businesses
- `GET /api/business/:id` - Get specific business
- `PUT /api/business/:id` - Update business profile
- `DELETE /api/business/:id` - Delete business
- `GET /api/business/owner/my-business` - Get owner's business

### Reviews & Ratings
- `POST /api/reviews` - Submit review
- `GET /api/reviews` - Get reviews

### Service Categories
- `GET /api/service-categories` - Get all categories
- `POST /api/service-categories` - Create category
- `PUT /api/service-categories/:id` - Update category
- `DELETE /api/service-categories/:id` - Delete category

### Messaging System
- Real-time messaging via Socket.IO
- Events: `send-message`, `typing-start`, `typing-stop`, `mark-read`, `delete-message`

### Complaints & Inquiries
- `POST /api/complaints` - Submit complaint
- `GET /api/complaints` - Get complaints
- `POST /api/inquiry` - Submit inquiry
- `GET /api/inquiry` - Get inquiries

## Security Features

- **Helmet.js**: Security headers and Content Security Policy
- **Rate Limiting**: 1000 requests per 15 minutes (configurable)
- **CORS Protection**: Configured for specific origins
- **Session Security**: Secure session management with MongoDB storage
- **Input Validation**: Comprehensive validation and sanitization
- **JWT Authentication**: Secure token-based authentication

## Real-Time Features

### Socket.IO Implementation
- **Real-time Messaging**: Instant message delivery
- **Typing Indicators**: Show when users are typing
- **Read Receipts**: Message read status tracking
- **User Status**: Online/offline status updates
- **Room Management**: Business-specific chat rooms

### Event Handling
- **Client Events**: `send-message`, `typing-start`, `typing-stop`, `mark-read`
- **Server Events**: `message-sent`, `new-message`, `user-typing`, `message-read`

## Design Philosophy

- **Mobile-First**: Responsive design optimized for mobile devices
- **Professional UI**: Clean, business-focused interface design
- **Consistent Branding**: Green color scheme throughout the platform
- **User Experience**: Intuitive navigation and user-friendly interactions
- **Accessibility**: Accessible design principles implementation

## Deployment

### Backend Deployment
- Set `NODE_ENV=production`
- Configure production MongoDB Atlas connection
- Set secure JWT and session secrets
- Use PM2 or similar process manager
- Configure production domain in `FRONTEND_URL`

### Frontend Deployment
- Build with `npm run build`
- Deploy `build/` directory to static hosting
- GitHub Pages deployment supported
- Configure production API endpoints

## Troubleshooting

### Common Issues
- **API Connection Issues**: Verify `FRONTEND_URL` matches frontend origin
- **Database Connection**: Check MongoDB connection string and network access
- **Email Not Working**: Verify Gmail App Password configuration
- **Socket.IO Errors**: Ensure CORS configuration matches frontend URL
- **Authentication Issues**: Check JWT secret and session configuration

### Health Checks
- `GET /` - API health status
- `GET /api/status` - Database and uptime status

## Contributing

We welcome contributions to improve AAA Services Directory! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

For major changes, please open an issue first to discuss the proposed changes.

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## Author

**BS IT Group # 08**

**Group Members:**
- **Ahsan Fareed** - Contact: [Email](mailto:mailtoahsanfareed@gmail.com) | [Github](https://github.com/ahsanfareed1) | [Upwork](https://www.upwork.com/freelancers/~01a9c1ff2d8b67a995)
- **Ali Haider**
- **Muhammad Ali**

**Project:** Accredited Assistance Association (AAA)  
**Role:** Full-Stack Development Team

---

*Accredited Assistance Association (AAA) - Bridging the gap between service providers and customers in Pakistan through technology and innovation.*<



