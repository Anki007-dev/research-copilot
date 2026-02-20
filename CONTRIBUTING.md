# Contributing to Research Copilot

Thank you for considering contributing to Research Copilot! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

Please be respectful and inclusive. All contributors are expected to maintain professional and courteous communication.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in [Issues](https://github.com/Anki007-dev/research-copilot/issues)
2. If not, create a new issue with:
   - Clear title describing the bug
   - Detailed description of the problem
   - Steps to reproduce
   - Expected vs. actual behavior
   - Screenshots/logs if applicable
   - System information (OS, Python version, etc.)

### Suggesting Enhancements

1. Use [Issues](https://github.com/Anki007-dev/research-copilot/issues) to suggest features
2. Provide clear use cases and benefits
3. Include examples of how the feature would work

### Setting Up Development Environment

#### Prerequisites
- Python 3.9+
- Node.js 16+
- PostgreSQL 12+
- Git

#### Backend Setup

```bash
# Clone the repository
git clone https://github.com/Anki007-dev/research-copilot.git
cd research-copilot

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
cd backend
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your configuration

# Run migrations
alembic upgrade head

# Start development server
uvicorn app.main:app --reload
```

#### Frontend Setup

```bash
cd frontend
npm install
npm start  # Development server
```

### Development Workflow

1. **Create a Feature Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make Your Changes**
   - Write clean, readable code
   - Follow existing code style
   - Add comments for complex logic

3. **Write Tests**
   ```bash
   # Backend tests
   pytest backend/tests/
   
   # Frontend tests
   npm test -- --coverage
   ```

4. **Commit with Clear Messages**
   ```bash
   git commit -m "feat: add source search functionality"
   ```
   
   Use conventional commits:
   - `feat:` for new features
   - `fix:` for bug fixes
   - `docs:` for documentation
   - `style:` for formatting
   - `refactor:` for code restructuring
   - `test:` for tests
   - `chore:` for maintenance

5. **Push and Create Pull Request**
   ```bash
   git push origin feature/your-feature-name
   ```

### Pull Request Guidelines

1. **Before Submitting**
   - Ensure tests pass
   - Update documentation
   - Rebase on main branch
   - No merge conflicts

2. **PR Description Should Include**
   - Clear title
   - Description of changes
   - Related issue number (if applicable)
   - Testing notes
   - Screenshots/demo (for UI changes)

3. **Code Review Process**
   - At least 2 approvals required
   - Address all feedback
   - Be open to suggestions

## Coding Standards

### Python
- Follow PEP 8
- Use type hints
- Use docstrings for functions and classes
- Line length: 100 characters

### JavaScript/React
- Use ES6+ features
- Functional components preferred
- Use React hooks
- Component structure:
  ```
  components/
  ├── ComponentName/
  │   ├── ComponentName.jsx
  │   ├── ComponentName.module.css
  │   └── index.js
  ```

## Documentation

- Update README.md for user-facing changes
- Add API documentation for new endpoints
- Include examples for new features
- Keep docs in sync with code

## Community

- Join our [Discussions](https://github.com/Anki007-dev/research-copilot/discussions)
- Participate in design decisions
- Help review PRs
- Share feedback and ideas

## Questions?

Feel free to:
- Open an issue with `question` label
- Start a discussion
- Contact maintainers

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
