# Managing Packages With npm

This is the boilerplate code for the Managing Packages With npm Challenges. Instructions for working on these challenges start at https://www.freecodecamp.org/learn/back-end-development-and-apis/managing-packages-with-npm/


# 📦 Quick Guide: Package Versioning

Versioning is a crucial part of managing dependencies in a project. By understanding how versioning works, you can maintain project stability while still receiving safe updates.

---

## 🎯 What is Versioning?
Versioning in packages indicates the changes made to a piece of software. A common format used is:

```
MAJOR.MINOR.PATCH
```
- **MAJOR** – Major changes that may break compatibility with previous versions.
- **MINOR** – New features that remain backward compatible.
- **PATCH** – Bug fixes or small changes that are backward compatible.

---

## ✨ Important Symbols in Versioning

### 1. **Exact Version**
```
1.2.3 = 1.2.3
```
- Locks to the exact version **1.2.3**.
- No patch or minor updates will be received.
- Ideal if you need 100% stability and no sudden changes.

---

### 2. **Tilde (~) - Patch and Minor**
```
~1.2.3 = 1.2.x
```
- Allows **patch** updates within the same **minor** version.
- For example, `~1.2.3` will receive updates like `1.2.4`, `1.2.5`, etc., but **not** `1.3.0`.
- Suitable for receiving bug fixes without major changes.

---

### 3. **Caret (^) - Minor and Patch**
```
^1.2.3 = 1.x.x
```
- Allows **minor** and **patch** updates.
- For example, `^1.2.3` will receive updates like `1.3.0`, `1.4.5`, etc., but **not** `2.0.0`.
- Suitable if you want new features as long as they are within the same **major** version.

---

## 🔧 Example Usage in package.json
```json
"dependencies": {
  "express": "^4.17.1",
  "lodash": "~4.17.15",
  "axios": "0.21.1"
}
```
- **express**: Will receive updates for `4.x.x` but not `5.x.x`.
- **lodash**: Will receive updates for `4.17.x` but not `4.18.x`.
- **axios**: Will only receive version `0.21.1`.

---

## 🚀 Tips
- Use `^` for flexibility with new features.
- Use `~` to maintain stability with bug fixes only.
- Use exact versions (without symbols) if stability is the top priority.

By understanding this, you can better manage dependencies, maintain project stability, and receive relevant updates.

