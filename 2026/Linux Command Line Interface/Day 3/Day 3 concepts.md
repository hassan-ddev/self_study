# 🐧 Linux CLI — Day 3 Notes
## Data Processing with CLI Tools

---

## 1. `wc` — Count Things

**wc = Word Count** (counts more than just words)

```bash
wc -l file.txt        # Count lines
wc -w file.txt        # Count words
wc -c file.txt        # Count characters/bytes
wc file.txt           # All three at once
```

**Real use case:** Check how many rows a CSV has before loading it into Pandas.
```bash
wc -l transactions.csv
# Output: 1048576 transactions.csv  → 1 million rows
```

---

## 2. `cut` — Extract Columns

```bash
cut -d',' -f1 dataset.csv        # Extract column 1
cut -d',' -f1,3,5 dataset.csv    # Extract columns 1, 3, and 5
cut -d',' -f2-4 dataset.csv      # Extract columns 2 through 4
cut -d',' -f1 dataset.csv > ids.txt   # Save extracted column to new file
```

**Flags:**
| Flag | Meaning |
|---|---|
| `-d','` | Delimiter — tells cut how columns are separated |
| `-f1` | Field — which column number to extract |

> ⚠️ Column numbers start at **1**, not 0 (unlike Python indexing).
> ⚠️ Default delimiter is **Tab** — always specify `-d','` for CSV files.

---

## 3. `sort` — Sort Data

```bash
sort names.txt              # Alphabetical sort (default)
sort -n scores.txt          # Numerical sort
sort -r dataset.csv         # Reverse order
sort -t',' -k2 -n file.csv  # Sort CSV by column 2 numerically
sort -u values.txt          # Sort and remove duplicates
```

**Critical — always use `-n` for numbers:**

Without `-n`, sort treats numbers as text (wrong):
```
Text sort:    1, 10, 2, 20, 3
Numeric sort: 1, 2, 3, 10, 20  ← correct
```

---

## 4. `uniq` — Find Unique Values

```bash
sort file.txt | uniq              # Show unique lines only
sort file.txt | uniq -c           # Count occurrences of each value
sort file.txt | uniq -c | sort -rn  # Sort by frequency (most common first)
```

> ⚠️ Input **must be sorted first** — `uniq` only removes adjacent duplicates.
> If duplicates aren't next to each other, it misses them.
> Always pipe `sort` before `uniq`.

---

## 5. The Pipe `|` — Chaining Commands

The pipe passes the output of one command as input to the next.
Read left to right — each `|` hands the result forward.

```bash
# Count how many rows contain "Fraud"
grep "Fraud" transactions.csv | wc -l

# Top 5 most common categories in column 3
cut -d',' -f3 dataset.csv | sort | uniq -c | sort -rn | head -5

# Find unique countries from column 4
cut -d',' -f4 users.csv | sort | uniq
```

---

## 6. Key Rules

| Rule | Why it matters |
|---|---|
| Use `-n` with `sort` for numbers | Without it, numbers sort as text — wrong order, no error |
| Always `sort` before `uniq` | `uniq` only catches adjacent duplicates |
| `cut` columns start at 1, not 0 | `-f1` is first column |
| Always specify `-d','` for CSVs | Default delimiter is Tab, not comma |

---

*Linux CLI for Data Scientists · Day 3 · June 2026*
