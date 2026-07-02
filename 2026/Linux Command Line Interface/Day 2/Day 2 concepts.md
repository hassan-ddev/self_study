# 🐧 Linux CLI — Day 2 Notes
## File & Text Manipulation

---

## 1. Creating Files

```bash
touch file.txt        # Creates an empty file
                      # If file already exists, updates its timestamp only
```

---

## 2. Viewing Files

```bash
cat file.txt          # Print entire file to screen
less file.txt         # Page through large files (Q to quit, arrows to scroll)
head file.txt         # First 10 lines
head -n 20 file.txt   # First 20 lines specifically
tail file.txt         # Last 10 lines
tail -n 20 file.txt   # Last 20 lines specifically
tail -f server.log    # Follow a live file — prints new lines as they're added
```

> ⚠️ Never use `cat` on a large file (e.g. 2GB CSV) — it floods the terminal.
> Use `head` or `less` to peek safely.

**When to use `tail -f`:** When a script is running in the background and writing to a log file, `tail -f` lets you watch output live without re-running `cat`.

---

## 3. Writing to Files

```bash
echo "text" > file.txt    # Write to file — OVERWRITES existing content
echo "text" >> file.txt   # Append to file — KEEPS existing content, adds at end
```

**Critical distinction:**

| Operator | Behaviour |
|---|---|
| `>` | Overwrites — old content is deleted |
| `>>` | Appends — old content is kept |

**Write multiple lines at once:**
```bash
cat > experiment_notes.txt << EOF
Experiment: Churn Prediction
Date: 2026-06-30
Model: XGBoost
EOF
```

---

## 4. Searching Inside Files — `grep`

```bash
grep "word" file.txt         # Find lines containing "word"
grep -i "word" file.txt      # Case-insensitive search
grep -n "word" file.txt      # Show line numbers of matches
grep -r "word" folder/       # Search recursively through all files in folder
grep -v "word" file.txt      # Invert — show lines that do NOT match
grep -c "word" file.txt      # Count how many lines match
```

**Common combinations:**
```bash
grep -in "fraud" data.csv    # Case-insensitive + line numbers
grep -r "import pandas" ./projects/   # Find all files that import pandas
grep -c "NaN" dataset.csv    # Count rows with missing values
```

---

## 5. Key Rules

- `>` vs `>>` — one wrong character silently wipes your file
- Always use quotes for multi-word search patterns: `grep "model accuracy" results.txt`
- `-r` is required when grepping a folder — without it, subfolders are skipped
- `touch` on an existing file does **not** erase it — it only updates the timestamp

---

*Linux CLI for Data Scientists · Day 2 · June 2026*
