
## AI-Powered Code Review Assistant 

An intelligent code review platform that uses Large Language Models (Claude/GPT-4) to automatically analyze pull requests and provide detailed feedback on code quality, security vulnerabilities, and best practices.

## Features

- 🤖 **AI-Powered Analysis**: Leverages Claude Sonnet 4.5 and GPT-4 for intelligent code review
- 🔍 **Comprehensive Detection**: Identifies bugs, security issues, code smells, and performance problems
- 📊 **Real-time Dashboard**: Track review metrics and trends
- 🔗 **GitHub Integration**: Automatic PR review via webhooks
- 💾 **Persistent Storage**: PostgreSQL for data, Redis for caching
- 🎨 **Modern UI**: Clean React interface with TailwindCSS
- ### Backend
- **Framework**: FastAPI (Python)
- **Database**: PostgreSQL with SQLAlchemy ORM
- **Cache**: Redis
- **LLM APIs**: Anthropic Claude, OpenAI GPT-4
- **Authentication**: JWT tokens

### Frontend
- **Framework**: React 18
- **State Management**: Redux Toolkit
- **Styling**: TailwindCSS
- **Routing**: React Router v6
- **HTTP Client**: Axios

## Getting Started

### Prerequisites
- Docker & Docker Compose
- Python 3.11+
- Node.js 18+
- API keys for Claude and/or OpenAI

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ai-code-reviewer.git
cd ai-code-reviewer
```

2. **Set up environment variables**
```bash
cp backend/.env.example backend/.env
# Edit backend/.env and add your API keys
```

3. **Start with Docker Compose**
```bash
docker-compose up -d
```

4. **Access the application**
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Docs: http://localhost:8000/docs

### Manual Setup (without Docker)

**Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn src.main:app --reload
```

**Frontend:**
```bash
cd frontend
npm install
npm start
```

## Usage

1. **Register/Login**: Create an account or sign in
2. **Add Repository**: Connect your GitHub repositories
3. **Create Review**: Trigger manual review or set up webhooks
4. **View Results**: Check dashboard for metrics and detailed issue reports

## API Endpoints

- `POST /api/auth/register` - Register new user
- `POST /api/auth/token` - Login
- `GET /api/repositories/` - List repositories
- `POST /api/reviews/` - Create review
- `GET /api/reviews/{id}/issues` - Get review issues

## Project Structure

See the folder structure artifact for detailed organization.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details
