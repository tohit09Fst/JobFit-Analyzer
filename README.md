# JobFit Analyzer

A comprehensive AI-powered job interview preparation platform that analyzes job descriptions and resumes to provide personalized interview questions, skill gap analysis, and preparation plans.

## 🚀 Features

- **AI-Powered Analysis**: Uses Google Gemini AI to analyze job descriptions and generate relevant content
- **Resume Parsing**: Supports PDF resume uploads for detailed analysis
- **Interview Question Generation**: Creates both technical and behavioral interview questions with explanations
- **Skill Gap Identification**: Identifies missing skills and their severity levels
- **Preparation Plans**: Generates structured 7-day preparation plans
- **Match Score Calculation**: Provides percentage match between resume and job requirements
- **User Authentication**: Secure JWT-based authentication system
- **Responsive Design**: Modern React frontend with SCSS styling

## 🛠 Tech Stack

### Frontend
- **React 19** - Modern React with hooks and functional components
- **Vite** - Fast build tool and development server
- **React Router** - Client-side routing
- **SCSS** - Enhanced CSS with variables and nesting
- **Axios** - HTTP client for API calls
- **ESLint** - Code linting and formatting

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database with Mongoose ODM
- **Google Gemini AI** - AI-powered content generation
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **PDF-parse** - Resume PDF parsing
- **Puppeteer** - Web scraping capabilities
- **Zod** - Schema validation

## 📋 Prerequisites

- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- Google AI API key (for Gemini AI)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/tohit09Fst/JobFit-Analyzer.git
   cd JobFit-Analyzer
   ```

2. **Backend Setup**
   ```bash
   cd Backend
   npm install

   # Create .env file in Backend directory
   cp .env.example .env  # if exists, otherwise create manually
   ```

   Configure your `.env` file:
   ```env
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/jobfit-analyzer
   JWT_SECRET=your_jwt_secret_here
   GOOGLE_AI_API_KEY=your_google_ai_api_key_here
   ```

   Start the backend server:
   ```bash
   npm run dev
   ```

3. **Frontend Setup**
   ```bash
   cd ../Frontend
   npm install

   # Start the development server
   npm run dev
   ```

4. **Access the Application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:3000

## 📖 Usage

1. **Register/Login**: Create an account or login to access the platform
2. **Create Interview Analysis**:
   - Enter job title and description
   - Upload your resume (PDF format)
   - Optionally provide self-description
3. **Review Analysis**:
   - View match score
   - Study generated technical and behavioral questions
   - Identify skill gaps
   - Follow the preparation plan

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Interview Analysis
- `POST /api/interview/analyze` - Analyze job description and resume
- `GET /api/interview/reports` - Get user's interview reports
- `GET /api/interview/:id` - Get specific interview report
- `DELETE /api/interview/:id` - Delete interview report

## 🏗 Project Structure

```
JobFit-Analyzer/
├── Backend/
│   ├── src/
│   │   ├── config/          # Database configuration
│   │   ├── controllers/     # Route controllers
│   │   ├── middlewares/     # Authentication & validation
│   │   ├── models/         # MongoDB schemas
│   │   ├── routes/         # API routes
│   │   └── services/       # AI and utility services
│   ├── server.js           # Server entry point
│   └── package.json
├── Frontend/
│   ├── src/
│   │   ├── features/       # Feature-based components
│   │   │   ├── auth/       # Authentication pages
│   │   │   └── interview/  # Interview analysis pages
│   │   ├── App.jsx         # Main app component
│   │   └── app.routes.jsx  # Route configuration
│   ├── index.html
│   └── package.json
└── README.md
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Google Gemini AI for powering the analysis engine
- The open-source community for the amazing tools and libraries
- Contributors and users of the JobFit Analyzer platform

---

**Made with ❤️ for job seekers worldwide**
