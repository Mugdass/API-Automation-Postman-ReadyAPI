# 🔹 API-Automation-Postman-ReadyAPI

API automation using:
- ✅ **Postman** + **Newman CLI** (for CI/CD)
- ✅ **ReadyAPI** (for advanced, licensed local testing)

---

## 📁 Project Structure

postman/ → Postman collections
readyapi/ → Placeholder for ReadyAPI projects (not CI-compatible)
.github/workflows/ → GitHub Actions workflow



---

## 🚀 Running Postman Tests

Install Newman:

```bash
npm install -g newman


Run collection:

newman run postman/SampleCollection.json




🔁 CI/CD Integration

This project runs Postman API tests on push and pull request using GitHub Actions.
ReadyAPI tests are excluded from CI due to licensing.

✅ Workflow: .github/workflows/ci.yml


on: [push, pull_request]
jobs:
  postman-tests:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: npm install -g newman
      - run: newman run postman/SampleCollection.json




---

## 📄 `.gitignore` (optional)


node_modules/
*.log
.DS_Store
