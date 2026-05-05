# DeadCodeX - AI-Powered Code Analysis Platform
# DeadCodeX 🚀

An intelligent code error detection and rectification platform powered by AI. Upload your code, connect to cloud services, and get instant error analysis with AI-powered fixes.
DeadCodeX is an AI-powered automated dead code detection, code quality analysis, and cleanup platform designed to improve maintainability, reduce technical debt, and optimize software projects.

## Features
## 📌 Problem Statement

### 🚀 Core Capabilities
- **AI-Powered Error Detection**: Automatically detect errors, warnings, and code quality issues
- **Intelligent Code Rectification**: AI-suggested fixes with detailed explanations
- **Multi-Language Support**: JavaScript, TypeScript, Python, Java, Go, Rust, and more
- **Real-Time Analysis**: Get instant feedback on your code
Modern and legacy codebases often contain:

### 📤 Multiple Upload Sources
- **Manual Upload**: Drag and drop files or upload ZIP archives
- **GitHub Integration**: Clone and analyze repositories (placeholder - OAuth setup required)
- **Google Drive**: Import code from your Drive (placeholder - OAuth setup required)
- **AWS S3**: Connect to S3 buckets (placeholder - credentials required)
- Unused variables, imports, functions, and classes
- Duplicate logic
- Dead or unreachable code
- Poor code quality patterns
- Increasing build times
- Difficult maintenance

### 🛠️ Analysis Features
- Error and warning detection
- Code quality suggestions
- Best practice recommendations
- Language-specific analysis
- File-by-file breakdown

### 💾 Data Management
- Automatic backups before modifications
- Export cleaned code
- Backup history
- Settings management
These issues slow down development and increase technical debt.
## 💡 Solution

### Installation
DeadCodeX intelligently scans source code repositories, uploaded projects, or ZIP files using static analysis + AI-assisted detection to identify unnecessary code, quality issues, and optimization opportunities.

1. Clone the repository:
```bash
git clone <repository-url>
cd deadcodex
```
It then provides confidence-based cleanup recommendations.

2. Install dependencies:
```bash
bun install
```
---

3. Set up environment variables:
```bash
cp .env.example .env
```
## ✨ Features

Edit `.env` with your configuration:
```env
DATABASE_URL="file:./db/custom.db"
SESSION_SECRET="your-secret-key-here"
```
### 🚀 Core Features

4. Initialize the database:
```bash
bun run db:push
```
- 🔍 Detect dead code automatically
- 🤖 AI-powered code analysis
- 🧹 Cleanup recommendations
- 📊 Confidence scoring
- 📄 Export analysis reports
- ⚡ Improve project performance
- 📂 Repository scanning support
- 🔐 Secure uploads

5. Start the development server:
```bash
bun run dev
```
### 📤 Upload Sources

- Manual file upload
- ZIP project upload
- GitHub repository integration
- Cloud source support (future)

The application will be available at `http://localhost:3000`
### 🛠️ Analysis Features

## Usage
- Unused imports
- Unused variables
- Unused functions/classes
- Duplicate logic detection
- Unreachable code detection
- File-wise report generation
- Suggestions with severity levels

### 1. Sign Up
- Visit the homepage
- Click "Get Started"
- Sign up with email/password or OAuth (Google/GitHub)
---

### 2. Upload Code
- Go to the Upload page
- Choose your upload source:
  - **Files**: Drag and drop or browse for files
  - **GitHub**: Enter repository URL
  - **Drive**: Provide Google Drive URL
  - **AWS**: Enter bucket and key details
- Click "Start Analysis"
## 🛠 Tech Stack

### 3. Review Analysis
- View detected errors and warnings
- Read AI suggestions
- Preview original and rectified code
- Download individual files
### Frontend

### 4. Clean Up Code
- Select files to clean
- Click "AI Rectify" for automatic fixes
- Review the changes
- Download cleaned files
- HTML5
- Tailwind CSS
- JavaScript

### 5. Manage Settings
- Configure preferences
- Set backup frequency
- Choose default language
- Manage notifications
### Backend

## Project Structure
- Python Flask / Node.js

```
deadcodex/
├── prisma/
│   └── schema.prisma          # Database schema
├── src/
│   ├── app/
│   │   ├── analysis/[id]/    # Analysis result page
│   │   ├── cleanup/[id]/     # Code cleanup page
│   │   ├── dashboard/        # User dashboard
│   │   ├── login/            # Login page
│   │   ├── register/         # Registration page
│   │   ├── settings/         # Settings page
│   │   ├── upload/           # Upload page
│   │   └── api/              # API routes
│   ├── components/           # React components
│   ├── hooks/               # Custom hooks
│   └── lib/                 # Utilities and helpers
└── package.json
```
### Database

- SQLite / PostgreSQL

### Analysis Engine

- Python AST Parsing
- Rule Engine
- AI Suggestions

---

## 📁 Project Structure

```bash
DeadCodeX/
├── app.py
├── requirements.txt
├── package.json
├── templates/
│   ├── index.html
│   ├── dashboard.html
│   ├── upload.html
│   ├── analysis.html
│   └── settings.html
├── static/
│   ├── css/
│   └── js/
├── uploads/
├── reports/
└── instance/
## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user
- `GET /api/auth/session` - Get current session

### User
- `GET /api/user` - Get current user info

### Upload & Analysis
- `POST /api/upload` - Upload code for analysis
- `GET /api/scans` - List all scans
- `GET /api/scans/[id]` - Get scan details
- `POST /api/analyze` - Rectify code with AI

### Settings & Backup
- `GET /api/settings` - Get user settings
- `POST /api/settings` - Update settings
- `POST /api/backup` - Create backup
- `GET /api/backup` - List backups

## Technology Stack

- **Framework**: Next.js 16 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS 4
- **UI Components**: shadcn/ui (Radix UI primitives)
- **Database**: Prisma ORM with SQLite
- **Authentication**: Custom session-based auth
- **File Processing**: unzipper for ZIP extraction
- **Icons**: Lucide React
- **Animations**: Framer Motion
- **Notifications**: Sonner

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `DATABASE_URL` | Database connection string | `file:./db/custom.db` |
| `SESSION_SECRET` | Secret for session encryption | - |

## OAuth Configuration

To enable OAuth providers (Google, GitHub), add the following to your `.env`:

```env
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
GITHUB_CLIENT_ID="your-github-client-id"
GITHUB_CLIENT_SECRET="your-github-client-secret"
```

Then implement the OAuth callback handlers in `/src/app/api/auth/oauth`.

## Database Schema

### User
- Authentication (email, OAuth)
- Profile information
- OAuth tokens (encrypted)

### Settings
- User preferences
- Auto-cleanup settings
- Notification settings
- Backup configuration

### Scan
- Project information
- Analysis results
- Error and warning counts
- Source tracking (manual, GitHub, Drive, AWS)

### CodeAnalysis
- File-level analysis
- Error details
- Suggestions
- Original and rectified code

### Backup
- Backup history
- Export data
- Size and status

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details.

## Support

For issues and questions, please open an issue on GitHub.
# DeadCodeX
