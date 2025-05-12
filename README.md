# 🔁 Recursive File and Folder Renamer for Flutter Feature Modules

This Python script helps you **quickly rename entire feature folders and files** in a Flutter Clean Architecture project by **recursively replacing a keyword** (e.g., `register`) with a new one (e.g., `login`) in all file and folder names.

---

## 🧠 Why Use This?

When building Flutter apps with **Clean Architecture**, features are often organized into self-contained modules like:

```
features/
├── login/
│   ├── data/
│   ├── domain/
│   └── presentation/
```

When duplicating an entire feature module (e.g., copying `register` to create a new `login` feature), this tool saves you time by auto-renaming:

- `register_bloc.dart` → `login_bloc.dart`
- `register_event.dart` → `login_event.dart`
- `register_state.dart` → `login_state.dart`
- `register_model.dart` → `login_model.dart`
- `register_repository.dart` → `login_repository.dart`
- `register_datasource.dart` → `login_datasource.dart`
- `register_entity.dart` → `login_entity.dart`
- `register_usecase.dart` → `login_usecase.dart`

📁 These files typically reside under:
- `lib/features/<feature>/presentation/`
- `lib/features/<feature>/data/`
- `lib/features/<feature>/domain/`

This script will help you rename all such file **names**

---

## ⚙️ Configuration

Open the script and edit these two variables:

```python
OLD_WORD = "register"        # Word to replace
NEW_WORD = "login"     # Replacement word
```

---

## 🚀 How to Run

1. Make sure Python 3 is installed.
2. Place this script in the root of your Flutter project.
3. Run:

```bash
python rename_recursive.py
```

4. Preview the files/folders to be renamed.
5. Confirm with `y` to proceed.

---

## 📁 What It Does

- Recursively traverses the directory tree.
- Replaces all occurrences of `OLD_WORD` with `NEW_WORD` in:
  - Folder names
  - File names
- Leaves file **contents unchanged** (you can do that using search-replace in IDE after renaming structure).

---

## ❗ Note

- This tool **does not modify the contents** of the files (e.g., class names, function names, string literals).
- These files (like `register_bloc.dart`, `register_event.dart`, etc.) are **not included** in this repository. This script is intended to assist after you duplicate a real feature module in your own Flutter project.
- Always **review and test your code** after running the script to ensure all identifiers are updated correctly.
- ✅ **Tip:** Use IDE refactoring tools or search-and-replace to update class names and contents inside the files.

---

## 👨‍💻 Author

**Muhammed Iqbal** – [LinkedIn](https://linkedin.com/in/iqbaltld)
