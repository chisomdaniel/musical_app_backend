# 🛠️ Contribution Guidelines for `musical_app_backend`

## 📁 Project Structure
- Keep all Django apps inside the `/apps` directory.
- Group files logically within each app: `models.py`, `serializers.py`, `views.py`, `urls.py`, etc.
- Reusable utilities, mixins, and helpers should go in a `utils/` directory.

---

## ✅ Getting Started
1. **Clone the Repository**
   ```bash
   git clone https://github.com/chisomdaniel/musical_app_backend.git
   cd musical_app_backend
   ```

2. **Set Up Virtual Environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Run Migrations & Server**
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

---

## 🔃 Git Workflow
- Use the `dev` branch for development. `prod`/`staging` is always deployable.
- Never commit directly to `dev` branch. Always user feature branches and make PR to `dev`
- Feature branches should follow naming convention:  
  ```
  feature/audio-conversion
  bugfix/user-authentication
  refactor/music-cleanup
  ```

### Merge Process
1. Create a PR to `dev` with a **clear title and description**.
2. Ensure all checks/tests pass.
3. At least **1 code review approval** is required before merging.

---

## 🧪 Testing
- Write unit tests for all new functionality in `tests/` inside each app.
- Run all tests before pushing:
  ```bash
  python manage.py test
  ```

---

## 🧼 Code Style & Formatting
- Follow **PEP8** standards.

---

## 📄 Commit Message Format
Use the conventional commit format:
```
<type>: <short summary>

[optional body with explanation]
```

Examples:
```
feat: add audio upload endpoint
fix: handle audio file format errors
docs: update README with setup steps
```

---

## 📚 Documentation
- Update docstrings for all models, views, and complex logic.
- Proper code commenting for specific sections is encouraged

---

## 📦 Dependencies
- Always add new packages to `requirements.txt` using pip freeze:
  ```bash
  pip freeze > requirements.txt
  ```

---

## 🔐 Secrets & Security
- Never commit `.env` files or credentials.
- Use environment variables for secrets and keys.
- Add `.env` and `*.pyc` to `.gitignore`.

---

## 🤝 Communication
- Use issues or tasks to describe bugs, feature requests, or suggestions.
- Before starting a major feature, confirm architecture with the team lead or via an issue thread.

