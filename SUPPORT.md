# 💬 Support & Getting Help

Thank you for using QuantumShift! We're here to help. Here's how to get support.

---

## 🚀 Quick Links

| Resource | Purpose | Link |
|----------|---------|------|
| 📚 Documentation | Full guides and tutorials | [docs/](../docs/) |
| 💬 Discussions | Q&A with community | [GitHub Discussions](https://github.com/orgs/Quantum-Shift-app/discussions) |
| 🐛 Bug Reports | Report issues | [GitHub Issues](https://github.com/issues) |
| 🔒 Security Issues | Report vulnerabilities | [SECURITY.md](SECURITY.md) |
| 📧 Contact | General inquiries | support@quantum-shift.fr |

---

## 🎯 Getting Help

### 1. **Search First** 🔍

Before asking, please:

- [ ] Check the [documentation](../docs/)
- [ ] Search [existing discussions](https://github.com/orgs/Quantum-Shift-app/discussions)
- [ ] Search [existing issues](https://github.com/issues)
- [ ] Check the [Troubleshooting Guide](../docs/troubleshooting.md)

### 2. **GitHub Discussions** (Recommended for Questions)

Perfect for:
- General questions
- Setup help
- Best practices
- Feature requests
- Discussions with the community

**How to post:**

1. Go to [GitHub Discussions](https://github.com/orgs/Quantum-Shift-app/discussions)
2. Click "New Discussion"
3. Choose a category:
   - **💬 General**: General questions
   - **🆘 Help**: Need assistance
   - **🎓 Show & Tell**: Share your work
   - **💡 Ideas**: Suggest improvements

4. Use a clear, descriptive title
5. Add relevant details:
   ```
   **Product**: QuantumShift AI v4.2
   **OS**: macOS 14.2
   **Python**: 3.10.11

   **Question**: How do I...?
   ```

### 3. **GitHub Issues** (For Bugs & Features)

Use for:
- Bug reports
- Feature requests
- Documentation improvements

**How to create:**

1. Click "New Issue" in the relevant repo
2. Choose the appropriate template:
   - 🐛 Bug Report
   - ✨ Feature Request
   - 📚 Documentation
   - 🔒 Security

3. Fill out all required fields
4. Be as detailed as possible

### 4. **Email Support**

For:
- Enterprise support
- Confidential issues
- Account troubles
- Partnership inquiries

**Email**: support@quantum-shift.fr

**Response Time**:
- Priority 1 (Critical): 4 hours
- Priority 2 (High): 24 hours
- Priority 3 (Medium): 48 hours
- Priority 4 (Low): 1 week

---

## 📋 Support Matrix

| Issue Type | Channel | Response Time | Contact |
|-----------|---------|----------------|---------|
| **Bug Report** | GitHub Issues | 24-48 hours | issues@your-repo |
| **Feature Request** | Discussions/Issues | 48-72 hours | discussions@github |
| **Security** | Email (PRIVATE) | 24 hours | security@quantum-shift.fr |
| **Documentation** | GitHub Issues | 48-72 hours | issues@your-repo |
| **General Question** | Discussions | 48 hours | discussions@github |
| **Enterprise** | Email | 4 hours | support@quantum-shift.fr |
| **Partnership** | Email | 1-2 weeks | contact@quantum-shift.fr |

---

## 🛠️ Troubleshooting Self-Help

### Common Issues

**Q: App crashes on startup**
- Check Python version: `python --version` (need 3.10+)
- Check dependencies: `pip install -r requirements.txt`
- Check environment: `python src/main.py --check-env`
- See: [Troubleshooting Guide](../docs/troubleshooting.md)

**Q: Database connection failed**
- Check PostgreSQL is running: `psql --version`
- Check connection string in `.env`
- Run migrations: `alembic upgrade head`
- See: [DB Setup Guide](../docs/development/database.md)

**Q: "Permission denied" error**
- Check file permissions: `chmod +x scripts/*.sh`
- Check API token in `.env`
- Check GitHub token if using GitHub API
- See: [Security Guide](../docs/security/authentication.md)

**Q: Tests failing**
- Run setup: `pytest --setup-show`
- Check test requirements: `pip install -e ".[dev]"`
- Run single test: `pytest tests/test_specific.py -v`
- See: [Testing Guide](../docs/development/testing.md)

### More Help

- 📚 [Full Documentation](../docs/)
- 🔧 [Troubleshooting Guide](../docs/troubleshooting.md)
- 🏗️ [Architecture Overview](../docs/architecture/)
- 👨‍💻 [Development Guide](../docs/development/)

---

## 💡 How to Ask for Help Effectively

### ✅ DO

- ✓ Search before asking
- ✓ Provide minimal reproducible example
- ✓ Include error messages and logs
- ✓ Specify version and environment
- ✓ Be clear and descriptive
- ✓ Use proper formatting (code blocks)
- ✓ Be patient and respectful

### ❌ DON'T

- ✗ Post same question in multiple channels
- ✗ Include sensitive information (keys, passwords)
- ✗ Request private support for public issues
- ✗ Use ALL CAPS
- ✗ Be rude or demanding
- ✗ Bump old threads unless critical new info

### Example Good Question

```markdown
**Title**: [HELP] Quantum algorithm crashes with > 10 qubits

**Environment**:
- OS: macOS 14.2 (M3 Pro)
- Python: 3.10.11
- QuantumShift: v4.2
- PennyLane: 0.33.1

**Problem**:
When running QAOA with 11+ qubits, I get memory error

**Steps to reproduce**:
1. Create circuit with 12 qubits
2. Run optimizer.run_qaoa(iterations=100)
3. Observe crash

**Error**:
```
MemoryError: Unable to allocate 4.2 GiB for array
```

**Things tried**:
- Increased swap space (didn't help)
- Ran on different machine (same issue)
- Works fine with 10 qubits

**Question**: Is this a known limitation? Any workarounds?
```

---

## 🤝 Community Support

The QuantumShift community is helpful and welcoming!

- Join [GitHub Discussions](https://github.com/orgs/Quantum-Shift-app/discussions)
- Follow [@QuantumShiftApp](https://twitter.com/quantum_shift)
- Read our [Blog](https://blog.quantum-shift.fr)
- Check [Case Studies](https://quantum-shift.fr/case-studies)

---

## 🆘 Critical Issues

If you experience:
- 🔴 Data loss
- 🔴 Security breach
- 🔴 Complete service outage
- 🔴 Critical vulnerability

**Please contact immediately:**
```
📞 Emergency: +33 1 XX XX XX XX
📧 Email: security@quantum-shift.fr (urgent in subject)
📱 Slack: #critical-issues (if you're in our Slack)
```

---

## 📈 Escalation Path

1. **Self-help**: Docs, FAQ, Troubleshooting
2. **Community**: Discussions, GitHub Issues
3. **Support Team**: Email (support@quantum-shift.fr)
4. **Engineering**: Critical issues, deep dives
5. **C-Level**: Enterprise partnerships, escalations

---

## 💬 Feedback

We'd love to hear from you!

- **Feature ideas?** → Discussions → Ideas
- **Something wrong?** → Issues → Bug Report
- **Documentation unclear?** → Issues → Documentation
- **General feedback?** → Email support@quantum-shift.fr

---

**Thank you for being part of the QuantumShift community! 🌌✨**

*Last updated: March 2026*
