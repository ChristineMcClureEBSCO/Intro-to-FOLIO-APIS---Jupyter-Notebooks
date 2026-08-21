# Setting Up Python & Jupyter Notebooks in VS Code

This guide has two parts:

- **Part 1: Quick Start** — a condensed checklist for people who've coded before and just need the order of operations.
- **Part 2: Detailed Steps** — full instructions for people who have never coded before, with fuller explanations.

**A note on computer access:** You'll need local admin access on the computer you're using to install Python and VS Code. If this is a work computer and you don't have admin rights, check with your IT department before starting — without it, the installers in Steps 1 and 2 may fail or be blocked.

**A note on accuracy:** Software interfaces change over time. These steps reflect how VS Code, Python, and the relevant extensions work as of mid-2026, but menu names or button positions may look slightly different by the time you read this. If a step doesn't match what you see on screen, that's the most likely reason.

**A note on the repository link:** The notebooks live at `https://github.com/ChristineMcClureEBSCO/Intro-to-FOLIO-APIS---Jupyter-Notebooks`. All files sit in the root of the repo (no subfolders), including:
- `README.md`
- `fines and fees report.ipynb`
- `folio-notebooks-requirements.txt`
- `folio_auth.ipynb`
- `folio_auth_test.ipynb`
- `instance records creation stats.ipynb`
- `shelf list by location.ipynb`

**Suggested order for running the notebooks:** You will need to first edit the settings in `folio_auth.ipynb` to include your FOLIO login credentials and tenant information. When that is complete, run the `folio_auth_test.ipynb` notebook. This is a short script to confirm you authenticated correctly, before moving on to any of the report notebooks.

---

## Part 1: Quick Start

For readers already comfortable with Python, git, and code editors. Order of operations only — see Part 2 for explanations.

1. Install Python 3.10+ from [python.org/downloads](https://www.python.org/downloads/) (Windows: check "Add Python to PATH").
2. Install [VS Code](https://code.visualstudio.com/).
3. In VS Code, install the [**Python**](https://marketplace.visualstudio.com/items?itemName=ms-python.python) and [**Jupyter**](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) extensions (both published by Microsoft).
4. Close or download the notebooks from:
   - Go to `https://github.com/ChristineMcClureEBSCO/Intro-to-FOLIO-APIS---Jupyter-Notebooks`
5. Open in VS Code.
6. Open a terminal in VS Code (**Terminal > New Terminal**) and run:
   ```
   pip install -r folio-notebooks-requirements.txt
   ```
7. Open `folio_auth.ipynb` first to enter your FOLIO credentials, then `folio_auth_test.ipynb` to confirm authentication works. After that, open whichever report notebook you need (`fines and fees report.ipynb`, `instance records creation stats.ipynb`, `shelf list by location.ipynb`).
8. Select a kernel (top-right of the notebook) — pick the Python interpreter you just installed the requirements into. Install `ipykernel` if prompted.
9. Run cells individually (▶ on each cell) or use **Run All**.

If anything above is unfamiliar, jump to the matching step in Part 2.

---

## Part 2: Detailed Steps

A step-by-step guide for people new to coding. Follow these steps in order — don't skip ahead.

### What you'll end up with

By the end of this guide you'll have:
1. Python installed on your computer
2. VS Code (a free code editor) installed
3. Two VS Code extensions installed (Python and Jupyter)
4. The FOLIO notebooks downloaded to your computer
5. The ability to open a `.ipynb` notebook file, install the required libraries, and run code in it

---

### Step 1: Install Python

1. Go to **[python.org/downloads](https://www.python.org/downloads/)**.
2. Click the big yellow "Download Python" button (it will detect your operating system automatically).
3. Run the installer you downloaded.
   - **Windows:** On the very first install screen, check the box that says **"Add Python to PATH"** before clicking Install. This step is easy to miss and causes problems later if skipped.
   - **Mac:** Python 3 is often pre-installed on Macs, but it's frequently an older version. It's fine to install a fresh copy from python.org — it won't conflict with the system version.
4. To confirm it worked, open a terminal:
   - **Windows:** Open the **Command Prompt** (search for it in the Start menu).
   - **Mac:** Open **Terminal** (search for it with Spotlight, Cmd+Space).
5. Type this and press Enter:
   ```
   python3 --version
   ```
   (On some Windows setups it may be `python --version` instead — try that if the first doesn't work.)
6. If you see something like `Python 3.12.4`, it worked. Any Python 3.10 or newer is fine for most notebooks.

---

### Step 2: Install VS Code

1. Go to **[code.visualstudio.com](https://code.visualstudio.com/)**.
2. Click the download button for your operating system.
3. Run the installer and accept the default options.
4. Open VS Code once installation finishes.

---

### Step 3: Install the Python and Jupyter extensions

VS Code doesn't understand Python or Jupyter notebooks out of the box — you add that ability with extensions.

1. In VS Code, look at the icons running down the far left side of the window. Click the one that looks like four squares (it's called the **Extensions** icon). Keyboard shortcut: `Ctrl+Shift+X` (Windows) or `Cmd+Shift+X` (Mac).
2. In the search box at the top of that panel, type **Python**.
3. Find the extension called **Python**, published by **Microsoft** (it should be the top result, with a blue checkmark). Click **Install**.
4. Now search for **Jupyter** in the same search box.
5. Find the extension called **Jupyter**, also published by **Microsoft**. Click **Install**.
   - Installing Jupyter usually pulls in the Python extension automatically if you hadn't already installed it, but it doesn't hurt to have done both manually.

---

### Step 4: Download the FOLIO notebooks

The notebooks live in a public GitHub repository, so anyone with the link can download them.

1. Go to: `https://github.com/ChristineMcClureEBSCO/Intro-to-FOLIO-APIS---Jupyter-Notebooks`
2. You have two options for getting the files onto your computer:

   **Option A — Download as a ZIP (simpler, no extra software needed):**
   - Click the green **Code** button near the top of the page.
   - Click **Download ZIP**.
   - Find the downloaded ZIP file (usually in your Downloads folder) and extract/unzip it. On Windows, right-click it and choose **Extract All**. On Mac, just double-click it.
   - Remember where you extracted it — you'll open this folder in VS Code next.

   **Option B — Clone with git (if you already have git installed):**
   - Open a terminal (see Step 1 for how).
   - Navigate to where you want the folder to live, e.g.:
     ```
     cd Documents
     ```
   - Run:
     ```
     git clone https://github.com/ChristineMcClureEBSCO/Intro-to-FOLIO-APIS---Jupyter-Notebooks.git
     ```
   - This creates a new folder with the repository's contents.

All the files you need — including `folio-notebooks-requirements.txt` and every notebook — sit directly in the root of the downloaded folder, so no need to hunt through subfolders.

**A quick note on which notebook to open first:** Once everything's installed (Steps 5–7 below), open `folio_auth.ipynb` before any of the others — that's where you'll enter your FOLIO login credentials. Then run `folio_auth_test.ipynb` to confirm you authenticated successfully. Only after that should you move on to the report notebooks (`fines and fees report.ipynb`, `instance records creation stats.ipynb`, or `shelf list by location.ipynb`).

---

### Step 5: Open the folder in VS Code

1. In VS Code, go to **File > Open Folder**.
2. Select the folder you extracted or cloned in Step 4 — the one that contains the notebook file(s) and `folio-notebooks-requirements.txt`.
3. If VS Code asks whether you trust the authors of this folder, click **Yes, I trust the authors**.

---

### Step 6: Open a terminal inside VS Code

You'll use this to install the required libraries.

1. Go to the menu bar: **Terminal > New Terminal**.
2. A terminal panel will open at the bottom of the VS Code window. This is the same kind of terminal you used in Step 1, just built into the editor.

---

### Step 7: Install the required libraries

1. In the terminal you just opened, type:
   ```
   pip install -r folio-notebooks-requirements.txt
   ```
   and press Enter.
2. You should see text scrolling by as it downloads and installs each library. This can take anywhere from a few seconds to a few minutes depending on how many libraries are listed and your internet speed.
3. If you get an error saying `pip` is not recognized, try `pip3 install -r folio-notebooks-requirements.txt` instead.
4. If you get a "permission denied" type error, try:
   ```
   pip install -r folio-notebooks-requirements.txt --user
   ```
5. If you get a "file not found" error, double check you're in the right folder and that the requirements file is actually named and located where you expect — see the note at the end of Step 4.

**I'm not certain which exact error message your system will show if something goes wrong** — error text varies by operating system and Python version. If you hit an error not covered here, copy the exact error text and search for it, or ask for help with the exact message.

---

### Step 8: Open a notebook

1. In the **Explorer** panel on the left (the file list), click on the `.ipynb` file you want to open.
2. VS Code will display it as a notebook: a series of "cells" you can run one at a time, rather than as a plain text file.

---

### Step 9: Select a kernel

The "kernel" is the Python environment that will actually run your code.

1. In the top-right corner of the notebook, you'll see a button (it may say **Select Kernel**, or show a Python version number if one is already chosen).
2. Click it.
3. Choose **Python Environments**, then select the Python version you installed in Step 1.
4. If you're prompted to install something called `ipykernel`, click **Install** — this is a small, standard package required to connect Python to the notebook and is expected the first time you do this.

---

### Step 10: Run the notebook

1. Hover over a code cell — a small **play (▶) button** appears on its left edge.
2. Click it to run that cell.
3. The output (if any) appears directly below the cell.
4. Repeat for each cell, top to bottom, or use **Run All** from the toolbar at the top of the notebook to run every cell in order.

---

### Quick troubleshooting

| Problem | Likely fix |
|---|---|
| `python3` or `pip` "not recognized" | Python wasn't added to PATH — reinstall Python and check that box (Windows), or use `python`/`pip` instead of `python3`/`pip3` |
| No "Select Kernel" option appears | The Jupyter extension may not have installed correctly — check the Extensions panel to confirm it's installed and enabled |
| A library import fails even after installing requirements | Confirm the kernel you selected in Step 9 is the same Python environment where you ran `pip install` in Step 7 — mismatched environments is the most common cause of this |

---

### Appendix: Using a terminal outside VS Code

Sometimes it's easier to troubleshoot Python itself *outside* of VS Code first, to rule out whether a problem is with Python or with VS Code. This uses the same kind of terminal from Step 1, not the one built into VS Code.

**Windows:**
1. Click the Start menu (or press the Windows key) and type `Command Prompt`.
2. Click on **Command Prompt** in the results to open it.
   - Alternative: type `PowerShell` instead — either works for the commands in this guide.

**Mac:**
1. Press `Cmd+Space` to open Spotlight search.
2. Type `Terminal` and press Enter.

**Linux:**
1. This varies by desktop environment, but a common shortcut is `Ctrl+Alt+T`. If that doesn't work, look for "Terminal" in your applications menu.

#### Things to check in this standalone terminal if something isn't working

1. **Confirm Python is installed and on PATH:**
   ```
   python3 --version
   ```
   or
   ```
   python --version
   ```
   If both give a "not recognized" / "command not found" error, Python either isn't installed or wasn't added to PATH during install (see Step 1's Windows note). The fix is usually to reinstall Python and make sure the "Add Python to PATH" box is checked.

2. **Confirm pip is installed and working:**
   ```
   pip3 --version
   ```
   or
   ```
   pip --version
   ```
   This should print a version number and a file path. Pip is normally installed automatically alongside Python, so if `python3` works but `pip3` doesn't, that's a signal something went wrong during the Python install — reinstalling Python is usually the simplest fix.

3. **Check which Python you're actually using**, if you have multiple versions installed (this can happen if you installed Python more than once, or have both a Mac system Python and a python.org Python):
   ```
   which python3
   ```
   (Mac/Linux) or
   ```
   where python3
   ```
   (Windows). This tells you the exact file path being used. It matters because the "kernel" you select in VS Code (Step 9) needs to point to the same Python installation where you ran `pip install -r folio-notebooks-requirements.txt` — otherwise VS Code will look for libraries in the wrong place and report them as missing even though you installed them.

4. **Try the install command here directly**, if it failed inside VS Code:
   ```
   cd path/to/your/folder
   pip3 install -r folio-notebooks-requirements.txt
   ```
   Replace `path/to/your/folder` with the actual folder containing `folio-notebooks-requirements.txt` (you can usually drag the folder into the terminal window to auto-fill its path on Mac and Linux). Running it here isolates whether the problem is with pip/Python itself, or something specific to how VS Code's built-in terminal is configured.

**I want to flag:** the exact wording of error messages and terminal behavior can vary a fair amount between Windows, Mac, and Linux, and even between versions of the same OS. The steps above cover the most common cases I'm aware of, but I can't guarantee they'll match every reader's exact setup — if someone hits an error not described here, the most reliable next step is to search for the exact error text.

---

*This guide covers the standard setup path as of when it was written. If you're following it much later and something looks different on screen, the general sequence (install Python → install VS Code → add Python + Jupyter extensions → download notebooks → open folder → install requirements → select kernel → run cells) should still hold, but I'd recommend double-checking against VS Code's own current documentation at code.visualstudio.com if a specific button or menu name doesn't match. The repo's file layout was confirmed directly by the repo owner at the time of writing — if files are added, removed, or renamed later, this guide won't automatically reflect that.*
