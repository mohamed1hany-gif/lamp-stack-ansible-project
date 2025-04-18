# Ansible LAMP Stack Deployment

## 📌 Objective
Automate the deployment and configuration of a LAMP stack (Linux, Apache, MySQL, PHP) on multiple servers using Ansible, following best practices for structure, modularity, and maintainability.

---

## 🧱 Project Structure & Best Practices

This project follows Ansible best practices:
- **Roles** are used to separate concerns (e.g., apache, mysql, php, firewall).
- **Blocks** are used for logically grouped tasks and to implement error handling.
- **Includes/imports** ensure playbooks are modular and easy to manage.
- **Error handling** is implemented using `block`, `rescue`, and `always` sections.
- **Handlers** notify and restart services such as Apache when configurations change.

---

## ⚙️ Functional Requirements

- ✅ Install and configure **Apache** web server.
- ✅ Deploy a sample `index.php` page to verify web server functionality.
- ✅ Install and **secure MySQL**:
  - Set root password
  - Remove test database
  - Remove anonymous users
  - Disable remote root login
- ✅ Install **PHP** and validate Apache can process PHP files.

---

## 🎁 Extras (Bonus Features)

- 🔥 Configure **UFW (Uncomplicated Firewall)** to allow HTTP (port 80) and HTTPS (port 443).
- 🧪 Use a **separate inventory** file to support multiple environments such as:
  - `dev`
  - `prod`

