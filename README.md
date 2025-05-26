# incluse-a11y

> A developer-first accessibility diagnostic and checklist tool tailored for inclusive digital products in the Indian public sector and beyond.

---

## ✨ What is incluse-a11y?

**incluse-a11y** is a lightweight, CLI-based and CI-friendly tool that checks basic accessibility issues in your frontend codebase. It helps you:

- Catch missing alt texts, ARIA labels, and poor color contrasts.
- Generate a simple Markdown or JSON report.
- Use in GitHub/GitLab CI pipelines as a **warning**, not an error.
- Maintain accessibility visibility without slowing dev velocity.

---

## 🧩 Features

- ✅ Alt text check for `<img>`
- ✅ Missing `aria-label`, `aria-labelledby` detection
- ✅ Detect low contrast text elements
- ✅ `accessibility-checklist.md` status parser
- 🧪 Easily extendable rule engine
- 🛠 CI/CD friendly output

---

## 🚀 Getting Started

### 1. Install locally

```bash
npm install -g incluse-a11y
```

### 2. Run accessibility scan

```bash
incluse-a11y scan ./path/to/your/project
```

### 3. Output warning report

```bash
incluse-a11y scan ./src --report markdown > a11y-report.md
```

---

## 🔧 How to Use in GitHub/GitLab CI

### GitHub Actions Example:

```yaml
- name: Run Accessibility Scan
  run: |
    npx incluse-a11y scan ./src > a11y-report.md

- name: Report Warnings
  run: |
    if grep -q '\[ \]' a11y-report.md; then
      echo "⚠️ Accessibility issues found. See a11y-report.md"
    fi
```

> ⚙️ Want to fail builds on critical issues only? Configure with `--strict` flag.

---

## 🛠 Roadmap

- [ ] Add keyboard navigation tree checker
- [ ] Support for Indian regional language detection
- [ ] Mobile-first view and TalkBack tagging
- [ ] YAML/JSON custom rule definitions

---

## 🤝 Contributing

We welcome PRs and suggestions! Follow our `CONTRIBUTING.md` for guidelines.

---

## 📄 License

MIT License © 2025 incluse-a11y team
