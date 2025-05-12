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

To save time, you might **copy an existing feature** (like `register`) and then reuse it for another similar feature (like `login`). However, manually renaming all files and folders can be tedious and error-prone.

This script automates that for you!

---

## ✨ Example Use Case

Suppose you want to create a `login` feature based on an existing `register` feature. Just set:

```python
OLD_WORD = "register"
NEW_WORD = "login"
```

Then run the script. It will rename all relevant files and folders such as:

```
login_bloc.dart       → register_bloc.dart  
login_repository.dart → register_repository.dart  
features/register/       → features/login/
```

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

- This only renames file and folder **names**, not the content inside the files.
- Always **review and test** your code after the rename.
- Recommended to commit your work or back up before running.

---

## 👨‍💻 Author

**Muhammed Iqbal** – [LinkedIn](https://linkedin.com/in/iqbaltld)
