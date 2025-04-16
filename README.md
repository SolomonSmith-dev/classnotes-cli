# 📝 ClassNotes CLI

Take and manage class notes straight from your terminal — fast, organized, and distraction-free.

This project includes two CLI tools:

- `classnote`: Take a new note using your terminal editor  
- `classnotes`: List, open, and search notes by subject  

> 💡 Notes are saved under:  
> `~/.class_notes/<subject>/<timestamp>.txt`

---

## ⚙️ Features

- 📌 One-line note creation from anywhere in terminal  
- 📁 Automatically organized by subject and timestamp  
- 🔍 Search all your notes  
- 📖 Instantly open the latest note  
- 💾 Offline, lightweight, and portable  

---

## 📥 Installation

### 🔨 Manual Setup

**1. Clone the repository:**

```bash
git clone https://github.com/SolomonSmith-dev/classnotes-cli.git
cd classnotes-cli
```

**2. Make the scripts executable:**

```bash
chmod +x classnote classnotes
```

**3. Create a `~/bin` folder if it doesn't exist and symlink the scripts:**

```bash
mkdir -p ~/bin

ln -s "$PWD/classnote" ~/bin/classnote
ln -s "$PWD/classnotes" ~/bin/classnotes
```

**4. Add `~/bin` to your PATH (if it’s not already):**

- **For Zsh (macOS default):**

```bash
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

- **For Bash:**

```bash
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

---

### 💡 Optional One-Liner Setup (if `setup.sh` is added later)

```bash
curl -s https://raw.githubusercontent.com/SolomonSmith-dev/classnotes-cli/main/setup.sh | bash
```

---

## 🚀 Usage

**Create a new note:**

```bash
classnote cse2130
```

_Example: Saves a file like:_  
`~/.class_notes/cse2130/2025-04-15-14-30.txt`

---

**List all notes for a class:**

```bash
classnotes cse2130
```

---

**Open the latest note:**

```bash
classnotes cse2130 --latest
```

---

**Search for a keyword:**

```bash
classnotes cse2130 --search binary
```

---

## 📁 File Structure

```text
~/.class_notes/
├── math/
│   ├── 2025-04-15-09-30.txt
│   └── 2025-04-15-11-45.txt
├── cse2130/
│   ├── 2025-04-15-14-32.txt
│   └── 2025-04-15-15-47.txt
└── ssci/
    └── 2025-04-15-17-10.txt
```

---

## 💡 Pro Tips

**Change your default terminal editor (e.g., nano, vim, micro):**

```bash
export EDITOR="nano"
```

**Back up your notes manually:**

```bash
tar -czf class_notes_backup.tar.gz ~/.class_notes
```

---

## 🔮 Future Features (Ideas)

- `--open <filename>`: open any specific note  
- `--summary`: show the first line of each note  
- Git/Nextcloud syncing  
- Terminal dashboard or web frontend  

---

## 📄 License

MIT — use it, share it, hack it, ship it.

---

## 👨‍💻 Author

Made with 💻 and ☕ by [Solomon Smith](https://github.com/SolomonSmith-dev)


