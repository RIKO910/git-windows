# 🧰 Git Installation & SSH Configuration Guide

This guide will help you install Git, configure your identity, and set up SSH keys for GitHub on Windows.

---

## 🛠️ Step 1: Install Git

Download and install Git from the official website:  
👉 [https://git-scm.com/downloads](https://git-scm.com/downloads)

---

## 🧑‍💻 Step 2: Configure Git Global Username and Email

Open **Git Bash** and run the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
---

## 🔐 Step 3: Generate SSH Key (Windows)

Open Git Bash and run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Press Enter to accept the default file location (usually: C:\Users\YourUsername\.ssh\id_ed25519)
You can press Enter through all prompts unless you want to set a custom passphrase
Show the Public Key:

```bash
type C:\Users\YourUsername\.ssh\id_ed25519.pub
```

📋 Copy the entire output starting with ssh-ed25519

---

## 🔗 Step 4: Add SSH Key to GitHub
Login to your GitHub account

Go to Settings → SSH and GPG Keys → New SSH Key

Title: Any name (e.g., "My Laptop Key")

Key: Paste your copied SSH key

Click "Add SSH key"

✅ You're now set up to use Git and push/pull via SSH!

---

## 🧪 Optional: Test SSH Connection

Run this command:

```bash
ssh -T git@github.com
```

If successful, you'll see a message like:

```bash
Hi your_username! You've successfully authenticated.
```
