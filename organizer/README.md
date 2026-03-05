# 📂 Download Folder Organizer

It is too easy for a download folder to become a junk drawer.
This tool does one thing:

> Automatically organise your Downloads folder, by sorting all files into folders you define with a word.

It’s designed to be:

- safe (nothing moves unless you allow it)
- transparent (you see what will happen before it does)
- reversible (you can undo a run)
- boring in the right ways

---
### What does it do?

- Scans your downloads folder
- Classifies files based on configurable rules
- Creates destination folders if needed
- Moves files safely
- Skips locked or inaccessible files
- Logs everything it does
    
Optional:

- dry-run mode (see before anything moves)
- undo last run
    
### ⏯️ Usage

```bash
python organizer.py
```

Dry run (no files moved):

```bash
python organizer.py --dry-run
```

Undo last run:

```bash
python organizer.py --undo
```

---
#### ⚙️ Configuration

File rules live in a separate config file so you don’t need to touch the code.
> **Edit `file_rules.yaml` to define:**

- destination folders
- file extensions
- naming conventions

### Requirements

- Python 3.9+
- Works on macOS / Linux / Windows
    
#### 👮‍♀️ Safety notes

- Locked files are skipped
- Errors are logged, not fatal
- Dry-run is recommended on first use
- Undo only affects files moved by the last run
    
#### Status

Clarity and safety matter more than features.
This is a personal tool under active iteration.  
(currently the script only moves files created more than a week ago..looking forward to find an easy way to iterate this option)

#### Folder structure

organizer/
├── organizer.py
├── config/
│   └── file_rules.yaml
├── core/
│   ├── classifier.py
│   ├── mover.py
│   ├── undo.py
│   └── logger.py
├── logs/
├── README.md
