# 🚀 Create CS-Cart Addon

A **PHP CLI tool** to quickly scaffold a **CS-Cart addon** with a correct folder structure, namespaces, and boilerplate files.

> No Node.js required.  
> Works on **Windows**, **Linux**, and **macOS**.

---

## ✨ Features

- 📦 Generates CS-Cart–compatible addon structure
- 🧩 PSR-4 autoloading
- 🧠 Proper namespaces based on addon name
- 🛡 Validates addon name (`letters, numbers, underscore`)
- ⚡ Fast CLI execution
- 🌍 Cross-platform (Windows / Linux / macOS)

---

## 📁 Generated Structure

```text
my_addon/
├── app/
│   └── addons/
│       └── my_addon/
│           ├── controllers/
│           ├── models/
│           ├── schema/
│           ├── src/
│           │   ├── HookHandlers/
│           │   ├── Bootstrap.php
│           │   ├── Installer.php
│           │   └── ServiceProvider.php
│           └── addon.xml
├── design/
│   └── templates/
│       └── addons/
│           └── my_addon/
└── var/
    └── langs/
        └── addons/
````

---

## 📦 Installation

### ✅ Option 1: Install globally via Composer (recommended)

```bash
composer global require yourname/create-cscart-addon
```

Make sure Composer global bin is in your PATH:

```bash
# Linux / macOS
export PATH="$HOME/.composer/vendor/bin:$PATH"

# Windows (add manually)
C:\Users\YourUser\AppData\Roaming\Composer\vendor\bin
```

---

### ✅ Option 2: Local usage (no global install)

```bash
php bin/create-cscart-addon my_addon
```

---

## ▶️ Usage

```bash
create-cscart-addon price_update
```

Or (Windows / local):

```bash
php create-cscart-addon.php price_update
```

---

## 🧪 Validation Rules

### ✔ Allowed

```text
price_update
my_addon_123
```

### ❌ Not allowed

```text
price-update
price update
price@update
```

---

## 🧩 Files Generated

### `addon.xml`

* Autoload (PSR-4)
* Bootstrap
* Installer
* Active status

### `Bootstrap.php`

* Registers service provider
* Hook handler support

### `Installer.php`

* Install / uninstall lifecycle
* CS-Cart compliant

### `ServiceProvider.php`

* Dependency container support (Pimple)

---

## 🖥 Platform Notes

### Windows

* No `chmod` required
* Composer generates `.bat` automatically

### Linux / macOS

```bash
chmod +x bin/create-cscart-addon
```

---

## 🛠 Requirements

* PHP **8.0+**
* Composer
* CS-Cart **4.x+**

---

## 🗺 Roadmap

* [ ] Interactive mode
* [ ] `--force` overwrite flag
* [ ] Auto-detect CS-Cart root
* [ ] Hook handler generator
* [ ] Unit tests
* [ ] Symfony Console integration

---

## 🤝 Contributing

PRs are welcome.

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

## 📄 License

MIT License

---

## ⭐ Why this tool?

CS-Cart addon development lacks a **standard scaffold generator**.
This tool brings **Laravel-level developer experience (DX)** to CS-Cart.

---

```
