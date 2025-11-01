# Contributing to Cerno Docs

Thank you for your interest in contributing to Cerno Docs! We welcome contributions from the community.

## 🌟 How to Contribute

### Reporting Bugs
- Check if the bug has already been reported in [Issues](https://github.com/cerno-ai/cerno-docs/issues)
- If not, create a new issue with:
  - Clear title and description
  - Steps to reproduce
  - Expected vs actual behavior
  - System information (OS, Python version, GPU/CPU)
  - Relevant logs or error messages

### Suggesting Features
- Open an issue with the `enhancement` label
- Describe the feature and its use case
- Explain how it aligns with the project's goals

### Pull Requests

#### Before Starting
1. Fork the repository
2. Create a new branch from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

#### Development Setup
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   cd frontend && npm install
   ```

2. Set up your `.env` file:
   ```bash
   cp .env.sample .env
   # Add your API keys
   ```

3. Run the application:
   ```bash
   # Backend
   uvicorn api.main:app --reload

   # Frontend (in another terminal)
   cd frontend && npm run dev
   ```

#### Code Standards
- **Python**: Follow PEP 8, use type hints
- **TypeScript/React**: Follow existing code style
- **Formatting**: Run linting scripts in `scripts/` folder before committing:
  ```bash
  # Windows
  scripts\format.bat
  scripts\lint.bat

  # Linux/Mac
  ./scripts/format.sh
  ./scripts/lint.sh
  ```

#### Commit Messages
Follow conventional commits format:
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `refactor:` Code refactoring
- `test:` Adding or updating tests
- `chore:` Maintenance tasks

Example:
```
feat: Add support for PowerPoint presentations
fix: Resolve CUDA memory overflow on large documents
docs: Update installation instructions for Windows
```

#### Pull Request Process
1. Update documentation if needed (README, INSTALLATION.md)
2. Add tests for new functionality
3. Ensure all tests pass
4. Update CHANGELOG.md (if it exists)
5. Create a Pull Request with:
   - Clear description of changes
   - Link to related issues
   - Screenshots/GIFs for UI changes
   - Test results

### Areas We Need Help With
- 📝 **Documentation**: Improve tutorials, add examples
- 🐛 **Bug Fixes**: Check open issues
- ✨ **Features**: See roadmap in README.md
- 🧪 **Testing**: Add unit/integration tests
- 🌍 **Localization**: Multi-language support
- ⚡ **Performance**: Optimization improvements

## 🔧 Development Tips

### Testing Your Changes
```bash
# Test backend
pytest tests/

# Test frontend
cd frontend && npm run test
```

### Debugging
- Use `--reload` flag for hot-reloading during development
- Check logs in `qa_log.log` for backend issues
- Use browser DevTools for frontend debugging

### Common Gotchas
- GPU/CPU compatibility: Test both modes
- Large file processing: Consider memory limits
- API rate limits: Handle gracefully
- Cross-platform: Test on Windows/Linux/Mac if possible

## 📜 Code of Conduct

### Our Standards
- Be respectful and inclusive
- Welcome newcomers
- Accept constructive criticism
- Focus on what's best for the community

### Unacceptable Behavior
- Harassment or discriminatory language
- Trolling or insulting comments
- Personal or political attacks
- Publishing others' private information

## 🤝 Community

- **Discussions**: Use GitHub Discussions for questions
- **Issues**: For bugs and feature requests
- **Pull Requests**: For code contributions

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for making Cerno Docs better!** 🎉
