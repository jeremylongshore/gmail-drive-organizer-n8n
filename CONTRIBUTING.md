# Contributing to This Workflow

Thanks for your interest in contributing! This project welcomes contributions from everyone, whether you're fixing a typo, adding a feature, or improving documentation.

## How to Contribute

### Reporting Issues

If you find a bug or have a suggestion:

1. **Search existing issues** to avoid duplicates
2. **Open a new issue** with a clear title and description
3. **Include details**:
   - n8n version
   - Workflow version
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Error messages or screenshots

### Suggesting Features

We love new ideas! To suggest a feature:

1. **Check existing issues** to see if it's already proposed
2. **Open a feature request** with:
   - Clear description of the feature
   - Use case or problem it solves
   - Any implementation ideas you have
   - Examples of similar features (if applicable)

### Submitting Changes

#### Before You Start

1. **Fork the repository** to your GitHub account
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/your-username/[repo-name].git
   cd [repo-name]
   ```
3. **Create a branch** for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

#### Making Changes

1. **Test your changes** in n8n:
   - Import the modified workflow
   - Test all nodes and connections
   - Verify the workflow executes correctly
   - Check edge cases and error handling

2. **Update documentation** if needed:
   - README.md for user-facing changes
   - setup-guide.md for configuration changes
   - Comments in the workflow for complex logic

3. **Follow workflow best practices**:
   - Use descriptive node names
   - Add notes to complex nodes
   - Handle errors gracefully
   - Keep credentials separate from the workflow

#### Testing Checklist

Before submitting, verify:

- [ ] Workflow imports without errors
- [ ] All nodes are properly connected
- [ ] Credentials are parameterized (not hardcoded)
- [ ] Error handling works as expected
- [ ] Documentation is updated
- [ ] No sensitive data in the workflow file
- [ ] Workflow executes successfully with test data

#### Submitting a Pull Request

1. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add: Brief description of changes"
   ```

2. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

3. **Open a Pull Request**:
   - Go to the original repository
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template

4. **PR Description should include**:
   - What changes you made
   - Why you made them
   - How to test the changes
   - Any breaking changes
   - Screenshots (if UI changes)

### Commit Message Guidelines

Use clear, descriptive commit messages:

**Good examples**:
- `Add: Email notification node for errors`
- `Fix: Webhook authentication issue`
- `Update: Setup guide with OAuth instructions`
- `Refactor: Simplify data transformation logic`

**Format**:
```
Type: Brief description (50 chars or less)

Optional longer description explaining:
- Why this change is needed
- What problem it solves
- Any side effects or considerations
```

**Types**:
- `Add`: New feature or node
- `Fix`: Bug fix
- `Update`: Improvement to existing feature
- `Refactor`: Code reorganization
- `Docs`: Documentation changes
- `Test`: Testing improvements

## Code Review Process

1. **Maintainers will review** your PR
2. **Address feedback** if requested
3. **Make changes** in your branch and push
4. **PR will be merged** once approved

Typical review timeline: 3-7 days

## Development Setup

### Local Testing

1. **Install n8n locally**:
   ```bash
   npm install -g n8n
   ```

2. **Run n8n**:
   ```bash
   n8n start
   ```

3. **Import the workflow** at http://localhost:5678

4. **Make changes** and export when done:
   ```bash
   # Export from n8n UI: Workflows → Export
   # Save as workflow/workflow.json
   ```

### Workflow File Format

- Keep the workflow file **properly formatted JSON**
- Use **meaningful node names** (not "Node 1", "Node 2")
- Add **notes to complex nodes**
- Remove **personal credentials** before committing

### Documentation Standards

When updating docs:

- **Use clear, simple language**
- **Include examples** where helpful
- **Keep formatting consistent**
- **Test all code snippets**
- **Update table of contents** if adding sections

## Recognition

All contributors will be recognized:

- **Added to Contributors** section in README
- **Mentioned in release notes** for significant contributions
- **Credit in commit history**

## Questions?

Not sure about something? Ask!

- **Open an issue** with your question
- **Start a discussion** in GitHub Discussions
- **Tag it** with "question" label

We're here to help and want to make contributing easy.

## Code of Conduct

### Our Standards

- **Be respectful** and welcoming
- **Be collaborative** and constructive
- **Accept feedback** gracefully
- **Focus on the project**, not personal issues
- **Help others** when you can

### Unacceptable Behavior

- Harassment, discrimination, or personal attacks
- Trolling or insulting comments
- Publishing private information
- Spamming or off-topic discussions

### Enforcement

Violations may result in:
- Warning
- Temporary ban
- Permanent ban

Report issues to [maintainer email or contact method].

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

---

**Thank you for contributing!** Every improvement, no matter how small, makes this workflow better for everyone.
