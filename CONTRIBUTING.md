# Contributing to Jarvis

We welcome contributions! Please follow these guidelines to help us maintain code quality and project consistency.

## Code of Conduct

Be respectful, inclusive, and professional in all interactions.

## How to Contribute

### 1. Fork the Repository

```bash
git clone https://github.com/chriskxco/jarvis-quantum-bot.git
cd jarvis-quantum-bot
git remote add upstream https://github.com/chriskxco/jarvis-quantum-bot.git
```

### 2. Create a Feature Branch

```bash
git checkout -b feature/your-feature-name
# or for bug fixes:
git checkout -b fix/your-bug-fix
```

### 3. Make Your Changes

- Follow the existing code style
- Write clear, descriptive commit messages
- Add tests for new features
- Update documentation as needed

### 4. Test Your Changes

**Backend:**
```bash
cd backend
pytest
black --check .
flake8 .
mypy .
```

**Frontend:**
```bash
cd frontend
npm test
npm run lint
```

### 5. Commit and Push

```bash
git add .
git commit -m "Add feature: description of your changes"
git push origin feature/your-feature-name
```

### 6. Create a Pull Request

- Go to GitHub and create a PR from your branch to `main`
- Provide a clear description of your changes
- Reference any related issues

## Code Style

### Python (Backend)

- Follow PEP 8
- Use type hints
- Max line length: 88 characters
- Use black for formatting

```python
def process_message(message: str, use_quantum: bool = False) -> dict:
    """Process a message and return response."""
    # Implementation
    return {"response": "..."}
```

### JavaScript (Frontend)

- Follow ESLint configuration
- Use modern ES6+ syntax
- Use functional components with React hooks
- Add JSDoc comments for complex functions

```javascript
/**
 * Process audio data
 * @param {ArrayBuffer} audioData - The audio data to process
 * @returns {Promise<string>} Transcribed text
 */
async function transcribeAudio(audioData) {
  // Implementation
}
```

## Commit Message Guidelines

- Use clear, descriptive messages
- Start with a verb: Add, Fix, Update, Remove, etc.
- Keep the first line under 50 characters
- Add detailed explanation if needed

```
Add quantum algorithm optimization

- Improved circuit generation
- Added caching for repeated queries
- Reduced execution time by 40%
```

## Pull Request Guidelines

- Provide a clear description of changes
- Reference related issues with #issue-number
- Include before/after for visual changes
- Ensure all tests pass
- Request review from maintainers

## Development Setup

### Backend Development

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pip install -r requirements-dev.txt  # Add dev dependencies
pytest --cov  # Run tests with coverage
```

### Frontend Development

```bash
cd frontend
npm install
npm run dev  # Start dev server with hot reload
npm test  # Run tests
npm run build  # Build for production
```

## Testing

### Backend Tests

```bash
pytest
pytest --cov  # With coverage report
pytest -v  # Verbose output
pytest tests/test_quantum.py  # Specific test file
```

### Frontend Tests

```bash
npm test
npm test -- --coverage
npm test -- --watch
```

## Documentation

- Keep README.md up-to-date
- Document new features in API_DOCS.md
- Add code comments for complex logic
- Update INSTALLATION.md if setup changes

## Reporting Bugs

If you find a bug:

1. Check existing issues to avoid duplicates
2. Create a new issue with:
   - Clear title and description
   - Steps to reproduce
   - Expected vs actual behavior
   - Environment details (OS, Python/Node version, etc.)
   - Screenshots if applicable

## Feature Requests

We love feature ideas! Please:

1. Check existing issues first
2. Provide clear use case
3. Explain expected behavior
4. Suggest implementation if possible

## Areas for Contribution

We particularly welcome contributions in:

- **Quantum Algorithms**: Add new quantum circuits and algorithms
- **Speech Processing**: Improve audio handling and recognition
- **UI/UX**: Enhanced interface and user experience
- **Performance**: Optimization and caching improvements
- **Testing**: Additional test coverage
- **Documentation**: Better guides and examples

## Review Process

1. At least one maintainer review required
2. All tests must pass
3. Code must follow style guidelines
4. Documentation must be updated
5. PR will be merged after approval

## Questions?

- Open an issue on GitHub
- Check existing documentation
- Review previous discussions

Thank you for contributing to Jarvis! 🚀
