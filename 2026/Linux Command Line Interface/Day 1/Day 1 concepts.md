# 🐧 Linux CLI — Day 1 Notes
## Terminal Basics & File System Navigation

---

## 1. First Commands

```bash
whoami        # Show who is logged in
pwd           # Print current directory path (Print Working Directory)
date          # Show current date and time
echo "text"   # Print text to the screen
clear         # Clear the terminal screen
```

---

## 2. Getting Help

```bash
man ls        # Full manual for any command (Q to quit)
whatis grep   # One-line description of a command
ls --help     # Quick flag reference
```

---

## 3. Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Tab` | Auto-complete command or filename |
| `↑ / ↓` | Navigate command history |
| `Ctrl + C` | Kill a running process |
| `Ctrl + L` | Clear the screen |
| `Ctrl + R` | Search through command history |
| `Ctrl + A` | Jump to start of line |
| `Ctrl + E` | Jump to end of line |

---

## 4. The Linux File System

Unlike Windows (C:\), Linux has one root `/` and everything branches from it:

```
/
├── home/           ← Your personal files
│   └── hassan/
│       ├── datasets/
│       └── projects/
├── etc/            ← System config files
├── usr/            ← Installed programs
└── tmp/            ← Temporary files
```

---

## 5. Navigation Commands

```bash
ls              # List files in current directory
ls -l           # Detailed list (permissions, size, date)
ls -la          # Include hidden files (files starting with .)
ls -lh          # Human-readable file sizes (KB, MB, GB)

cd folder       # Move into a folder
cd ~            # Go to home directory
cd ..           # Go up one level
cd ../..        # Go up two levels
cd -            # Go back to previous directory

mkdir folder           # Create a directory
mkdir -p a/b/c         # Create nested directories at once
```

---

## 6. Key Rules

| Rule | Why it matters |
|---|---|
| Linux is case-sensitive | `Data.csv` and `data.csv` are two different files |
| Avoid spaces in filenames | Use `my_file.csv` not `my file.csv` — spaces break commands |
| `cd ../..` not `cd ....` | Each `..` is one level up, chained with `/` |
| `rm` has no Recycle Bin | Deleted files are gone permanently |

---

*Linux CLI for Data Scientists · Day 1 · June 2026*
